# Basic Employee Onboarding (AD)(RBAC)

## Problem Statement
Northstar Medical Group (NMG) is a fictional healthcare organization whose previous managed service provider (MSP) left its user accounts unorganized. NMG had no record of who had been hired, who had left, or who should have access to what. In healthcare, this creates HIPAA risk, since organizations must control access to patient information and make sure former employees don’t keep active accounts. My goal was to build an Active Directory environment with a clear OU structure and role-based security groups. I also wanted a repeatable process for adding users and giving them the right access.

## Solution Overview
I built a new Active Directory domain named NMG on a Windows Server domain controller to give the company a central, organized place to manage its users. I designed the structure around four departmental OUs: Finance, HR, IT, and Operations. For each OU, I created a matching security group (Finance-Users, HR-Users, IT-Users, and Operations-Users) and used a flat RBAC model, meaning each user belongs to one group that matches their job role, with no extra permissions. This kept access limited to what each role needs and made it easy to see who has access to what. I secured user provisioning by requiring a ticket request before creating any account, using a consistent naming convention (first initial plus last name, such as kmills), placing each user in the correct OU and security group at creation. To test the process, I simulated a ticket where a user had been placed in the wrong OU and group, then identified the mistake and corrected it.
## Video Walkthrough
[Add your video walkthrough link placeholder here. You will record this tomorrow and update this link so visitors can see a live demonstration of your lab environment.]

## Tools Used
* Windows Server
* Active Directory Domain Services
* VirtualBox
* UTM
* RBAC
* GitHub

## Project Timeline
* Day 1: Domain creation and domain controller promotion
* Day 2: Organizational unit and security group design
* Day 3: User provisioning and RBAC implementation
* Day 4: Incident response and resolution (NMG-0047)
* Day 5: Documentation and case study packaging

## Key Accomplishments
* Built NMG.com domain from scratch
* Solved a mock ticket where an user was given the incorrect access.
* I fully documented my steps end-to-end 
