# Potential Pitfalls
> Warning: The following are spoilers for the project. If you're stuck, you can use this as a reference.

## Step One: AWS EC2 Instance
- Public IP Address (if you don't set this up from the start, you have to configure it later)
- Security Group set-up

## Step Two: Log into EC2 Instance
- The cheating way: AWS EC2 Connect. The right way: SSH.
- 0.0.0.0 is really sus.
- Install Hugo :)

## Step Three: Running the site
- Why can't I see it? Because it's not running on the right port: `[URL]:1313/`
- Base URL and Bind: `hugo server -D --bind=0.0.0.0 --baseUrl=[URL]`
- VPC: Setting it up so it's publicly accessible

## Additional Pain Points
- If your repository is private, you need to set up git credentials on the EC2 instance.
- If you use AWS Linux, it doesn't come up with many things installed by default. You need to install git, hugo, etc.