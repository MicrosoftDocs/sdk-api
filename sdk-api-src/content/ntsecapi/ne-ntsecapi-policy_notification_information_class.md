---
UID: NE:ntsecapi._POLICY_NOTIFICATION_INFORMATION_CLASS
title: POLICY_NOTIFICATION_INFORMATION_CLASS
author: windows-sdk-content
description: The POLICY_NOTIFICATION_INFORMATION_CLASS enumeration defines the types of policy information and policy domain information for which your application can request notification of changes.
old-location: security\policy_notification_information_class.htm
tech.root: SecMgmt
ms.assetid: cf8eea7a-d3b0-4c3a-b05b-3027024ab025
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PPOLICY_NOTIFICATION_INFORMATION_CLASS, POLICY_NOTIFICATION_INFORMATION_CLASS, POLICY_NOTIFICATION_INFORMATION_CLASS enumeration [Security], PPOLICY_NOTIFICATION_INFORMATION_CLASS, PPOLICY_NOTIFICATION_INFORMATION_CLASS enumeration pointer [Security], PolicyNotifyAccountDomainInformation, PolicyNotifyAuditEventsInformation, PolicyNotifyDnsDomainInformation, PolicyNotifyDomainEfsInformation, PolicyNotifyDomainKerberosTicketInformation, PolicyNotifyMachineAccountPasswordInformation, PolicyNotifyServerRoleInformation, _lsa_policy_notification_information_class, ntsecapi/POLICY_NOTIFICATION_INFORMATION_CLASS, ntsecapi/PPOLICY_NOTIFICATION_INFORMATION_CLASS, ntsecapi/PolicyNotifyAccountDomainInformation, ntsecapi/PolicyNotifyAuditEventsInformation, ntsecapi/PolicyNotifyDnsDomainInformation, ntsecapi/PolicyNotifyDomainEfsInformation, ntsecapi/PolicyNotifyDomainKerberosTicketInformation, ntsecapi/PolicyNotifyMachineAccountPasswordInformation, ntsecapi/PolicyNotifyServerRoleInformation, security.policy_notification_information_class"
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
 - POLICY_NOTIFICATION_INFORMATION_CLASS
product: Windows
targetos: Windows
req.typenames: POLICY_NOTIFICATION_INFORMATION_CLASS, *PPOLICY_NOTIFICATION_INFORMATION_CLASS
req.redist: 
---

# POLICY_NOTIFICATION_INFORMATION_CLASS enumeration


## -description


The <b>POLICY_NOTIFICATION_INFORMATION_CLASS</b> enumeration defines the types of policy information and policy domain information for which your application can request notification of changes.


## -enum-fields




### -field PolicyNotifyAuditEventsInformation

Notify when any of the audited categories are changed.


### -field PolicyNotifyAccountDomainInformation

Notify when the account domain information changes.


### -field PolicyNotifyServerRoleInformation

Notify when the LSA server changes its role from primary to backup, or vice versa.


### -field PolicyNotifyDnsDomainInformation

Notify when the DNS domain information changes or if the primary domain information changes.


### -field PolicyNotifyDomainEfsInformation

Notify when the Encrypting File System (EFS) domain information changes.


### -field PolicyNotifyDomainKerberosTicketInformation

Notify when the Kerberos ticket for the domain changes.


### -field PolicyNotifyMachineAccountPasswordInformation

Notify when the machine account password changes.


### -field PolicyNotifyGlobalSaclInformation


### -field PolicyNotifyMax




## -see-also




<a href="https://msdn.microsoft.com/0c713d2b-e13a-44e0-8b48-68b233d1c562">LsaRegisterPolicyChangeNotification</a>



<a href="https://msdn.microsoft.com/c1000904-20a6-40db-9b59-2cbb79e00a67">LsaUnregisterPolicyChangeNotification</a>
 

 

