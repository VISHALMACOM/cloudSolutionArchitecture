# Cloud Solution Architecture
Cloud Practitioner and Cloud Solution Associate Exam Preparation Notes

# Practicals
# Concept1 - Web Application Using EC2 Instance
    • Create a new Amazon EC2 server instance from an existing server template.
    • Create a security group to restrict access to the server's resources.
    • Launch the instance.
    • Access the instance's Linux command-line interface directly, using a key pair for authentication.
      (Both .pem using VSCode and .ppk using Putty)
    • Associate an Elastic IP address with your Amazon EC2 instance.

# Concept2 - VPC's

    • Create an Amazon VPC.
    • Create public and private subnets.
    • Create an internet gateway.
    • Configure a route table and associate it to a subnet.
    • Create a public security group
    • Create an Amazon Elastic Compute Cloud (Amazon EC2) instance and make the instance publicly accessible.
    • Isolate an Amazon EC2 instance in a private subnet.
    • Create and assign security groups to Amazon EC2 instances.
    • Connect to Amazon EC2 instances using Session Manager, a capability of AWS Systems Manager

<img width="593" alt="image" src="https://github.com/VISHALMACOM/cloudSolutionArchitecture/assets/15323666/b3508b9a-03d1-4687-8d6a-1b87dca9cb53">

• Create an Amazon VPC.

     After creating a VPC, choose Actions and choose Edit VPC settings, enable DNS Hostnames.

     Any Amazon EC2 instances launched into this Amazon VPC now automatically receive a DNS hostname.

<img width="664" alt="image" src="https://github.com/VISHALMACOM/cloudSolutionArchitecture/assets/15323666/69c16446-e517-4e23-a1f9-de8ace80c78b">

• Create public and private subnets.

    Subnet name: Enter Public Subnet and choose the number of ips, you need by filtering with respect to the subnets.

    Example - If VPC IP Block 10.0.0.0/16(65532) ips get assigned, So, if you need 256 ips for public, 
              you can use 10.0.0.0/24(256) ips get assigned.
    Select Public Subnet, Choose Actions and choose Edit subnet settings, Select Enable auto-assign public IPv4 address,Choose Save.
    It is not yet public. It must have an internet gateway and route to the gateway to make it public.

    Subnet name: Enter Private Subnet and choose the number of ips, you need by filtering with respect to the subnets.
                 you can use 10.0.2.0/23(512) ips get assigned.[10.0.2.* - 10.0.3.*]

<img width="699" alt="image" src="https://github.com/VISHALMACOM/cloudSolutionArchitecture/assets/15323666/20ac4110-6e25-4bce-b458-c43f67412faf">
<img width="680" alt="image" src="https://github.com/VISHALMACOM/cloudSolutionArchitecture/assets/15323666/ae9649f6-642b-4773-9062-c87343cc87d3">

• Create an internet gateway.

    Choose Create internet gateway, You can now attach the internet gateway to your Lab VPC.
    From the same page, choose Actions and choose Attach to VPC. For Available VPCs, choose Lab VPC.
    Choose Attach internet gateway.
    Verify the state. It should display the following:
    State: Attached

<img width="872" alt="image" src="https://github.com/VISHALMACOM/cloudSolutionArchitecture/assets/15323666/3209dbd5-befc-471a-9526-91c6176135a9">


• Configure a route table and associate it to a subnet.

    Create a Public Route Table and Choose Lab VPC.
    Choose the Routes tab in the lower half of the page, Choose Edit routes and add route.
        Destination: Enter 0.0.0.0/0
        Target: Choose Internet Gateway in the dropdown menu and then choose the displayed internet gateway ID.
        Choose Save changes.
    Choose the Subnet Associations tab, Choose Edit subnet associations, Select Public Subnet, Choose Save associations.


<img width="877" alt="image" src="https://github.com/VISHALMACOM/cloudSolutionArchitecture/assets/15323666/86df7eff-ea64-4bb7-bc49-54651cf25cf8">



• Create a public security group

    Create Public SG, Select Lab VPC, In Inbound rules , Add rule of Anywhere HTTP.

<img width="885" alt="image" src="https://github.com/VISHALMACOM/cloudSolutionArchitecture/assets/15323666/7d49a4f5-0dae-467d-8fa1-2b579f9ce47b">

• Create an Amazon Elastic Compute Cloud (Amazon EC2) instance and make the instance publicly accessible.

    Launch an instance with Lab VPC, Public SG and make sure to run httpd service with ip address enabling.

• Isolate an Amazon EC2 instance in a private subnet.

• Create and assign security groups to Amazon EC2 instances.

• Connect to Amazon EC2 instances using Session Manager, a capability of AWS Systems Manager

# Concept4 - Elastic Load Balancing

    • Launching multiple EC2 web servers
    • Using bootstrapping techniques to configure Linux instances with Apache, PHP, and a simple PHP application downloaded from Amazon Simple Storage Service (S3).
    • Creating and configuring a load balancer that will sit in front of your Amazon EC2 web server instances.
    • Creating and configuring a Auto scaling group to make your application scalable and highly available
    • Viewing Amazon CloudWatch metrics for the load balancer.

![image](https://github.com/VISHALMACOM/cloudSolutionArchitecture/assets/15323666/056646ba-bd68-47be-90c0-7bf64134423e)







