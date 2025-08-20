
## Task Description
The task was to set up the following in AWS:

- Create a VPC with CIDR block `10.0.0.0/16`
- Attach an Internet Gateway (IGW) to the VPC
- Create a **Public Subnet** (`10.0.1.0/24`) with 256 IP addresses
- Create a **Private Subnet** (`10.0.2.0/24`) with 256 IP addresses
- Configure **Route Tables**:
  - Public Route Table → Internet Gateway → Public Subnet
  - Private Route Table → Private Subnet (no Internet access)
- Launch an **EC2 Linux instance** in the Public Subnet
- Verify connectivity by SSH into the instance

---

## Steps Performed
1. Created VPC with CIDR `10.0.0.0/16`
2. Created Internet Gateway and attached to VPC
3. Created Public Subnet (`10.0.1.0/24`) and enabled auto-assign public IP
4. Created Private Subnet (`10.0.2.0/24`)
5. Created Route Tables:
   - Public-RT → `0.0.0.0/0` → IGW → Public Subnet
   - Private-RT → Local VPC route only → Private Subnet
6. Launched EC2 instance (Amazon Linux 2023) in Public Subnet
7. Verified SSH access using PEM key

---

## Proof (Screenshots)

Screenshots are available in the [`/screenshots`](./screenshots) folder:

- VPC
- Internet Gateway
- Public Subnet
- Private Subnet
- Route Tables
- EC2 login (SSH successful)

---

## Tech Stack Used
- **AWS VPC**
- **AWS EC2**
- **Amazon Linux 2023**

---

✅ Task Completed Successfully  
