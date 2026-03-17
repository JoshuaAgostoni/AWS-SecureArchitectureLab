<h1>AWS-SecureArchitectureLab</h1>



<h2>Description:</h2>
This project demonstrates the design and deployment of a secure AWS cloud architecture using a custom Virtual Private Cloud (VPC). The environment was manually configured to showcase applied knowledge of network segmentation, least privilege IAM, logging, monitoring, and data protection best practices.


<h2>2.	Architecture Design:</h2>

Architecture Components:
* Custom VPC (10.0.0.0/16)
* Public Subnet (10.0.1.0/24)
* Private Subnet (10.0.2.0/24)
* Internet Gateway attached
* Public and Private Route Tables
* EC2 instance in public subnet
* IAM role with restricted permissions
* CloudTrail enabled (multi-region)
* GuardDuty enabled
* Secure S3 bucket with encryption and public access blocked
 


<h2>Environments Used: </h2>

<b>Amazon Web Services</b>

<h2>Program walk-through:</h2>

<p align="center">
Displays full architecture including VPC, public subnet, private subnet, and Internet Gateway attachment. <br/>
<a href="https://imgur.com/PcgMqP9"><img src="https://i.imgur.com/PcgMqP9.png" title="source: imgur.com" /></a>
<br />
<br />
Shows 0.0.0.0/0 route directed to the Internet Gateway, enabling internet access for public subnet resources  <br/>
<a href="https://imgur.com/QHvlH6B"><img src="https://i.imgur.com/QHvlH6B.png" title="source: imgur.com" /></a>
<br />
<br />
Displays SSH (Port 22) restricted to a trusted IP address instead of 0.0.0.0/0, enforcing least privilege network access <br/>
<a href="https://imgur.com/D5cZ53a"><img src="https://i.imgur.com/D5cZ53a.png" title="source: imgur.com" /></a>
<br />
<br />
Shows EC2 IAM role with AmazonS3ReadOnlyAccess attached. No administrative privileges granted.  <br/>
<a href="https://imgur.com/Uszfz8Z"><img src="https://i.imgur.com/Uszfz8Z.png" title="source: imgur.com" /></a>
<br />
<br />
Displays policy JSON defining read-only S3 permissions, demonstrating least privilege access control  <br/>
<a href="https://imgur.com/GXUms2J"><img src="https://i.imgur.com/GXUms2J.png" title="source: imgur.com" /></a>/>
<br />
<br />
Shows recorded API activity across the AWS account, providing auditing and forensic capability.  <br/>
<a href="https://imgur.com/nLOkQs9"><img src="https://i.imgur.com/nLOkQs9.png" title="source: imgur.com" /></a>
<br />
<br />
Confirms GuardDuty is enabled for continuous threat detection and anomaly monitoring.
<a href="https://imgur.com/NCYyUNI"><img src="https://i.imgur.com/NCYyUNI.png" title="source: imgur.com" /></a>
<br />
<br />
Displays 'Block All Public Access' enabled to prevent unintended data exposure.
<a href="https://imgur.com/w5Oatry"><img src="https://i.imgur.com/w5Oatry.png" title="source: imgur.com" /></a>
<br />
<br />
Shows server-side encryption enabled for data protection monitoring.
<a href="https://imgur.com/TTLb03c"><img src="https://i.imgur.com/TTLb03c.png" title="source: imgur.com" /></a>
<br />
<br />
Shows S3 Bucket set for logging configured monitoring.
<a href="https://imgur.com/264Uh5L"><img src="https://i.imgur.com/264Uh5L.png" title="source: imgur.com" /></a>
</p>

<h2>7.	Security Principles Demonstrated</h2>

* Network segmentation
* Principle of Least Privilege
* Defense in Depth
* Continuous monitoring and auditing
* Data encryption and access restriction
* AWS shared responsibility model awareness

