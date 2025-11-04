# Virtual-Internship
This is virtual internship done under the "Smart Internz" on the topic of "Streamlining Ticket Assignment for Efficient Support Operations" using ServiceNow
ServiceNow Virtual Internship Project

Project Title:
Streamlining Ticket Assignment for Efficient Support Operations

Category:
ServiceNow Application Developer

Skills Used:
User and Group Management
Flow Designer
Access Control Lists (ACLs)

Project Overview:
The objective of this project is to implement an automated system for ticket routing at ABC Corporation to improve operational efficiency. 
By accurately assigning support tickets to the appropriate teams, the system reduces delays in issue resolution, enhances customer satisfaction, 
and optimizes resource utilization within the support department.

Objectives:
• Automate the ticket routing process in ServiceNow
• Reduce manual workload and human error
• Improve response time and customer satisfaction
• Manage users, roles, and groups efficiently
• Implement security using ACLs

Implementation Steps:
1. User Creation
   - Created two users under System Security > Users.

2. Group Creation
   - Created two groups: Certificates Group and Platform Group.

3. Role Creation
   - Created two roles: Certification_Role and Platform_Role.

4. Table Creation
   - Created a table named "Operations Related" with issue fields.
   - Added issue choices such as:
     - Unable to login to platform
     - 404 error
     - Regarding certificates
     - Regarding user expired

5. Assign Roles and Users to Groups
   - Assigned Katherine Pierce to Certificates Group with Certification_Role.
   - Assigned Manne Niranjan to Platform Group with Platform_Role.

6. Assign Role to Table
   - For the u_operations_related table, added Platform_Role and Certification_Role 
     under read and write access.
   - Elevated role to security_admin when required.

7. Create ACLs
   - Created ACLs for restricting table field access.
   - Set admin role as the required role.

8. Create Flow for Automatic Ticket Assignment
   - Flow 1: Regarding Certificates
     - Trigger: Record created/updated in Operations Related table.
     - Condition: Issue = "Regarding Certificates"
     - Action: Assign ticket to Certificates Group.

   - Flow 2: Regarding Platform
     - Trigger: Record created/updated in Operations Related table.
     - Conditions: Issue = "Unable to login to platform" / "404 error" / "User expired"
     - Action: Assign ticket to Platform Group.

Results:
The automation successfully routed tickets to the correct groups based on issue type. 
Manual assignment was eliminated, improving accuracy and reducing response time. 
ACLs provided secure access control, and Flow Designer enabled easy low-code automation.

Conclusion:
The ServiceNow automation efficiently streamlined ticket routing, improved team productivity, 
and enhanced overall customer satisfaction. This demonstrates the power of ServiceNow’s 
low-code automation capabilities in optimizing IT service management operations.

References:
- ServiceNow Developer Documentation (developer.servicenow.com)
- ServiceNow Virtual Internship Materials
