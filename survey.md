# New company survey
This checklist is intended to help someone joining a new company (or possibly moving to a new department/role within a company) to gather and document crucial information early on.  It is intended that the checklist is copied to interal file storage before being completed - do not store your answers in this repo!

## macOS
- [ ] Are Macs enrolled in an MDM?
- [ ] What percentage are using the latest macOS major version?
- [ ] What percentage are using the latest macOS minor version?
- [ ] Is there any process in place to prompt users to upgrade?
- [ ] Is FileVault enabled?
  - [ ] Are recovery keys being escrowed?
  - [ ] Are recovery keys generally valid?
    - [ ] If not, consider deploying https://github.com/macadmins/escrow-buddy
- [ ] Is there an automated setup process?
  - [ ] Is the user kept informed about progress?
  - [ ] Are any errors reported back to IT?
- [ ] Are any users administrators on their Macs?
- [ ] Is there a process in place for assessing new macOS major (& minor?) versions?
  - [ ] Are there testing group(s) to check these versions for compatibility before deployment?
       
## macOS apps
- [ ] Is there a policy in place around what apps may be installed?
- [ ] Is a mechanism required to control which apps may be run?
  - [ ] Consider deploying https://github.com/google/santa
- [ ] Which apps are being centrally deployed/managed?
  - [ ] Are these apps up to date in the deployment tool?
    - [ ] If not, consider deploying https://github.com/autopkg/autopkg
  - [ ] Are these apps up to date on the Mac fleet?
    - [ ] If not, consider deploying https://github.com/munki/munki
  - [ ] Are there testing group(s) to check these apps for compatibility before deployment?

## Windows
- [ ] Are Windows PCs enrolled in an MDM?
- [ ] What percentage are using the latest Windows major version?
- [ ] What percentage are using the latest Windows minor version?
- [ ] Is there any process in place to prompt users to upgrade?
- [ ] Is Bitlocker enabled?
  - [ ] Are recovery keys being escrowed?
  - [ ] Are recovery keys generally valid?
- [ ] Is there an automated setup process?
  - [ ] Is the user kept informed about progress?
  - [ ] Are any errors reported back to IT?
- [ ] Are any users administrators on their Windows PCs?
       
## Windows apps
- [ ] Is there a policy in place around what apps may be installed?
- [ ] Is a mechanism required to control which apps may be run?
- [ ] Which apps are being centrally deployed/managed?
  - [ ] Are these apps up to date in the deployment tool?
    - [ ] If not, consider deploying https://github.com/autopkg/autopkg
  - [ ] Are these apps up to date on the Windows fleet?
  - [ ] Are there testing group(s) to check these apps for compatibility before deployment?

## Policies/procedures
- [ ] Is there an acceptable use policy governing what is/isn't allowed on company computers?
- [ ] Is there a BYOD policy governing what devices may be used to access company systems?
- [ ] Is there a device lifecycle policy governing when company computers should be eligible for replacement?

## IAM
- [ ] Where is the source of truth for employee data?
- [ ] Is there an SSO system for controlling access to apps?
  - [ ] Gain administrative access to the SSO system.
  - [ ] Are any significant apps not included in the SSO system?
  - [ ] Are service accounts present in the SSO system?
    - [ ] Are these accounts identifiable as such?
    - [ ] Are the uses of these service accounts documented?
  - [ ] Is administrative access to the SSO system appropriately limited?
  - [ ] Do changes from the HRIS flow into the SSO system?
  - [ ] Is there automation to automatically grant RBAC to apps?
  - [ ] Is there automation to automatically grant on-demand access to apps?
- [ ] Is there a documented process for user onboarding?
  - [ ] Are there any omissions from this process?
  - [ ] Are there any ways that the process could be (more) automated?
- [ ] Is there a documented process for user offboarding?
  - [ ] Are there any omissions from this process?
  - [ ] Are there any ways that the process could be (more) automated?

## Security tooling
- [ ] What security agents are being deployed to endpoints?
  - [ ] Gain administrative access to each security tool (as appropriate).
  - [ ] Are these agents kept up to date?
  - [ ] Is there any monitoring in place to identify inactive agents?
  - [ ] Are there any groups who get different configurations within these tools?
    - [ ] Are these groups documented?

## Asset Lifecycle 
- [ ] Is there an asset management tool/list?
  - [ ] Does it store purchase information?
    - [ ] Date?
    - [ ] Vendor?
    - [ ] Price?
  - [ ] Does it get automatically updated when an asset is reassigned?
- [ ] Is there provision for hardware repair?
  - [ ] What is the warranty duration?
- [ ] Are standard hardware models documented?
  - [ ] Are there any documented procedures for deviating from those models?

## MDM
- [ ] Gain administrative access to the/each MDM.
- [ ] Are there dev (& possibly non-prod) environments for each MDM?
- [ ] Are the access levels appropriate?
- [ ] Are there consistent naming conventions for policies/groups/profiles/scripts?
- [ ] Are configuration data being managed under version control?
- [ ] When does the Apple MDM cert need to be renewed?
  - [ ] Is this date recorded somewhere with appropriate notifications?
  - [ ] Are the account details recorded?
- [ ] When does the VPP token need to be renewed?

## Documentation
- [ ] Is there a centralised documentation store for IT?
  - [ ] Are there appropriate templates for the required documentation types?
  - [ ] Is the documentation generally up to date?

## Communication
- [ ] What are the preferred communication platforms?
  - [ ] General company announcements?
  - [ ] Company-wide IT announcements?
  - [ ] IT internal communications?
  - [ ] Team internal communications?
- [ ] Gain access to all relevant communication platforms.
- [ ] Have invites been received to all relevant recurring meetings?
- [ ] Has access been given to all email distribution groups?
- [ ] Has access been given to all group communication channels?

## Logging/alerting
- [ ] Is there a SIEM for centralised logging relating to IT systems?
  - [ ] Gain access to the SIEM.
  - [ ] Are logs being collected from MDM systems?
  - [ ] Are logs being collected from security tooling?
  - [ ] Are logs being collected from endpoints?
- [ ] Is there a centralised location for checking systems status/alerts?
  - [ ] Gain access to the status location.

## PKI
- [ ] Are PKI certs being deployed to endpoints?
  - [ ] Are all uses of the certs documented?
  - [ ] Are the individual certs automatically renewed?
  - [ ] When does the root CA cert expire?
  - [ ] Is there a mechanism for revoking individual certs?
