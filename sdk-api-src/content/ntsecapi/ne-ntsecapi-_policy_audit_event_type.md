---
UID: NE:ntsecapi._POLICY_AUDIT_EVENT_TYPE
title: "_POLICY_AUDIT_EVENT_TYPE"
author: windows-sdk-content
description: The POLICY_AUDIT_EVENT_TYPE enumeration defines values that indicate the types of events the system can audit.
old-location: security\policy_audit_event_type.htm
tech.root: secmgmt
ms.assetid: e8dbd1d5-37d5-4a97-9d1c-c645871dc7a5
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: "*PPOLICY_AUDIT_EVENT_TYPE, AuditCategoryAccountLogon, AuditCategoryAccountManagement, AuditCategoryDetailedTracking, AuditCategoryDirectoryServiceAccess, AuditCategoryLogon, AuditCategoryObjectAccess, AuditCategoryPolicyChange, AuditCategoryPrivilegeUse, AuditCategorySystem, POLICY_AUDIT_EVENT_TYPE, POLICY_AUDIT_EVENT_TYPE enumeration [Security], PPOLICY_AUDIT_EVENT_TYPE, PPOLICY_AUDIT_EVENT_TYPE enumeration pointer [Security], _POLICY_AUDIT_EVENT_TYPE, _lsa_policy_audit_event_type, ntsecapi/AuditCategoryAccountLogon, ntsecapi/AuditCategoryAccountManagement, ntsecapi/AuditCategoryDetailedTracking, ntsecapi/AuditCategoryDirectoryServiceAccess, ntsecapi/AuditCategoryLogon, ntsecapi/AuditCategoryObjectAccess, ntsecapi/AuditCategoryPolicyChange, ntsecapi/AuditCategoryPrivilegeUse, ntsecapi/AuditCategorySystem, ntsecapi/POLICY_AUDIT_EVENT_TYPE, ntsecapi/PPOLICY_AUDIT_EVENT_TYPE, security.policy_audit_event_type"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: ntsecapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ntsecapi.h
api_name:
 - POLICY_AUDIT_EVENT_TYPE
product: Windows
targetos: Windows
req.typenames: POLICY_AUDIT_EVENT_TYPE, *PPOLICY_AUDIT_EVENT_TYPE
req.redist: 
---

# _POLICY_AUDIT_EVENT_TYPE enumeration


## -description


The <b>POLICY_AUDIT_EVENT_TYPE</b> enumeration defines values that indicate the types of events the system can audit. The 
<a href="https://msdn.microsoft.com/2d543500-f639-4ef7-91f4-cdc5060dd567">LsaQueryInformationPolicy</a> and 
<a href="https://msdn.microsoft.com/2aa3b09e-2cd9-4a09-bfd6-b37c97266dcb">LsaSetInformationPolicy</a> functions use this enumeration when their <i>InformationClass</i> parameters are set to PolicyAuditEventsInformation.


## -enum-fields




### -field AuditCategorySystem

Determines whether the operating system must audit any of the following attempts:

<ul>
<li>Attempted system time change.</li>
<li>Attempted security system startup, restart, or shutdown.</li>
<li>Attempt to load extensible authentication features.</li>
<li>Loss of audited events due to auditing system failure.</li>
<li>Security log size that exceeds a configurable warning threshold level.</li>
</ul>

### -field AuditCategoryLogon

Determines whether the operating system must audit each time this computer validates the credentials of an account. Account logon events are generated whenever a computer validates the credentials of one of its local accounts. The credential validation can be in support of a local logon or, in the case of an Active Directory domain account on a domain controller, can be in support of a logon to another computer. Audited events for local accounts must be logged on the local security log of the computer. Account logoff does not generate an event that can be audited.


### -field AuditCategoryObjectAccess

Determines whether the operating system must audit each instance of user attempts to access a non-Active Directory object, such as a file,  that has its own system access control list (SACL) specified. The type of access request, such as Write, Read, or Modify, and the account that is making the request must match the settings in the SACL.


### -field AuditCategoryPrivilegeUse

Determines whether the operating system must audit each instance of user attempts to use  <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">privileges</a>.


### -field AuditCategoryDetailedTracking

Determines whether the operating system must audit specific events, such as program activation, some forms of handle duplication, indirect access to an object, and process exit.


### -field AuditCategoryPolicyChange

Determines whether the operating system must audit attempts to change <a href="https://msdn.microsoft.com/ba8c4f61-8cbc-4a36-8336-8a84d84b46e4">Policy</a> object rules, such as user rights assignment policy, audit policy, account policy, or trust policy.


### -field AuditCategoryAccountManagement

Determines whether the operating system must audit attempts to create, delete, or change user or group accounts. Also, audit password changes.


### -field AuditCategoryDirectoryServiceAccess

Determines whether the operating system must audit attempts to access the directory service. The Active Directory object has its own SACL specified. The type of access request, such as Write, Read, or Modify, and the account that is making the request must match the settings in the SACL.


### -field AuditCategoryAccountLogon

Determines whether the operating system must audit each instance of a user attempt to log on or log off this computer. Also audits logon attempts by privileged accounts that log on to the domain controller. These audit events are generated when the Kerberos <a href="https://msdn.microsoft.com/f17042c3-ba1a-408f-af55-5f171b0dee33">Key Distribution Center</a> (KDC) logs on to the domain controller. Logoff attempts are generated whenever the logon session of a logged-on user account is terminated.


## -remarks



The <b>POLICY_AUDIT_EVENT_TYPE</b> enumeration may expand in future versions of Windows. Because of this, you should not compute the number of values in this enumeration directly. Instead, you should obtain the count of values by calling 
<a href="https://msdn.microsoft.com/2d543500-f639-4ef7-91f4-cdc5060dd567">LsaQueryInformationPolicy</a> with the <i>InformationClass</i> parameter set to PolicyAuditEventsInformation and extract the count from the <b>MaximumAuditEventCount</b> member of the returned 
<a href="https://msdn.microsoft.com/3442e5e5-78cf-4bda-ba11-0f51ee40df16">POLICY_AUDIT_EVENTS_INFO</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/2d543500-f639-4ef7-91f4-cdc5060dd567">LsaQueryInformationPolicy</a>



<a href="https://msdn.microsoft.com/2aa3b09e-2cd9-4a09-bfd6-b37c97266dcb">LsaSetInformationPolicy</a>



<a href="https://msdn.microsoft.com/b734b5e8-1ee9-436b-b2a9-210ae79fbaf5">POLICY_INFORMATION_CLASS</a>
 

 

