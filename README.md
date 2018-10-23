## How To Create An AWS VPC Step By Step

1. Log in to AWS and click 'services' in the navbar.

2. Scroll down to 'Networking and Content Delivery' and select 'VPC'.

3. On the left side of the page select 'Elastic IPs'.

4. Click 'Allocate New Address' and then choose 'Allocate'. This will create an elastic IP address for your VPC.

5. Go back into VPC from the navbar (steps 1 and 2) and then click 'Launch VPC Wizard'.

6. On 'VPC With Public and Private Subnets', click 'Select'. This creates one isolated section within the AWS cloud that has direct access to the internet, and another that has no access to the internet (this is what you would use for a database).

7. On this next page, you can choose to name your VPC and subnet, in order to make them easier to identify in the console later. You can also specify your own IPv4 CIDR block ranges for the VPC and subnet if you'd like (IPv4 CIDR is just a way of showing your IP addresses along with the number of bits (shown in the suffix), e.g. 192.168.10.100/24). You can also change your availability zone if you so wish.

8. In the 'Specify the details of your NAT gateway' section, specify the allocation ID for the Elastic IP address in your account that you created in step 4. Then click 'Create VPC'.

9. Repeat steps 1 and 2, and then on the left side of the page select 'Security Groups'. On the page that pops up, select 'Create Security Group'.

10. Provide a name and description for your security group, then in 'VPC', type the ID of the VPC you created. Click 'Yes, Create'.

11. To create an instance of your VPC, under 'Services' in the navbar you must select 'EC2' and then click 'Launch Instance'.

12. Select your AMI of choice and then choose Next.

13. On the next page, in 'Network', select the VPC you created and then select a subnet. For example, launch a web server into the public subnet and the database server into the private subnet.

14. Click 'next' to proceed to the storage page (which you can edit if you so wish), and then click 'next' again to be taken to the Configure Security Group page.

15. Choose the 'Select an existing security group' option and select one of the security groups you created earlier. After this, launch the AMI normally as we have before.
