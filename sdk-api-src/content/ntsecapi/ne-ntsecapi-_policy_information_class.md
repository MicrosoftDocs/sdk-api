---
UID: NE:ntsecapi._POLICY_INFORMATION_CLASS
title: "_POLICY_INFORMATION_CLASS"
author: windows-driver-content
description: Defines values that indicate the type of information to set or query in a Policy object.
old-location: security\policy_information_class.htm
old-project: SecMgmt
ms.assetid: b734b5e8-1ee9-436b-b2a9-210ae79fbaf5
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: "*PPOLICY_INFORMATION_CLASS, POLICY_INFORMATION_CLASS, POLICY_INFORMATION_CLASS enumeration [Security], PPOLICY_INFORMATION_CLASS, PPOLICY_INFORMATION_CLASS enumeration pointer [Security], PolicyAccountDomainInformation, PolicyAuditEventsInformation, PolicyAuditFullQueryInformation, PolicyAuditFullSetInformation, PolicyAuditLogInformation, PolicyDefaultQuotaInformation, PolicyDnsDomainInformation, PolicyLsaServerRoleInformation, PolicyModificationInformation, PolicyPdAccountInformation, PolicyPrimaryDomainInformation, PolicyReplicaSourceInformation, _POLICY_INFORMATION_CLASS, _lsa_policy_information_class, ntsecapi/POLICY_INFORMATION_CLASS, ntsecapi/PPOLICY_INFORMATION_CLASS, ntsecapi/PolicyAccountDomainInformation, ntsecapi/PolicyAuditEventsInformation, ntsecapi/PolicyAuditFullQueryInformation, ntsecapi/PolicyAuditFullSetInformation, ntsecapi/PolicyAuditLogInformation, ntsecapi/PolicyDefaultQuotaInformation, ntsecapi/PolicyDnsDomainInformation, ntsecapi/PolicyLsaServerRoleInformation, ntsecapi/PolicyModificationInformation, ntsecapi/PolicyPdAccountInformation, ntsecapi/PolicyPrimaryDomainInformation, ntsecapi/PolicyReplicaSourceInformation, security.policy_information_class"
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
req.typenames: POLICY_INFORMATION_CLASS, *PPOLICY_INFORMATION_CLASS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Ntsecapi.h
api_name:
-	POLICY_INFORMATION_CLASS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# _POLICY_INFORMATION_CLASS enumeration


## -description


The <b>POLICY_INFORMATION_CLASS</b> enumeration  defines values that indicate the type of information to set or query in a <a href="https://msdn.microsoft.com/4253c7fb-85f5-441d-90bf-492e802ad0f8">Policy</a> object.


## -enum-fields




### -field PolicyAuditLogInformation

This value is obsolete.


### -field PolicyAuditEventsInformation

Query or set the auditing rules of the system. You can enable or disable auditing and specify the types of events that are audited. Use the 
<a href="https://msdn.microsoft.com/3442e5e5-78cf-4bda-ba11-0f51ee40df16">POLICY_AUDIT_EVENTS_INFO</a> structure.


### -field PolicyPrimaryDomainInformation

This value is obsolete. Use the <b>PolicyDnsDomainInformation</b> value instead. 
					


### -field PolicyPdAccountInformation

This value is obsolete.


### -field PolicyAccountDomainInformation

Query or set the name and SID of the account domain of the system. Use the 
<a href="https://msdn.microsoft.com/0e38ac5f-40db-405d-9394-b6bcb7c652b5">POLICY_ACCOUNT_DOMAIN_INFO</a> structure.


### -field PolicyLsaServerRoleInformation

Query or set the role of an LSA server. Use the 
<a href="https://msdn.microsoft.com/f66abe33-d8c8-45b8-9b94-d6890d786aaa">POLICY_LSA_SERVER_ROLE_INFO</a> structure.


### -field PolicyReplicaSourceInformation

This value is obsolete.


### -field PolicyDefaultQuotaInformation

This value is obsolete.


### -field PolicyModificationInformation

Query or set information about the creation time and last modification of the LSA database. Use the 
<a href="https://msdn.microsoft.com/ef4d1d1d-9b1b-4d67-80b8-2b548ec31a87">POLICY_MODIFICATION_INFO</a> structure.


### -field PolicyAuditFullSetInformation

This value is obsolete.


### -field PolicyAuditFullQueryInformation

This value is obsolete.


### -field PolicyDnsDomainInformation

Query or set Domain Name System (DNS) information about the account domain associated with a <a href="https://msdn.microsoft.com/4253c7fb-85f5-441d-90bf-492e802ad0f8">Policy</a> object. Use the 
<a href="https://msdn.microsoft.com/5b2879cf-e0dc-4844-bfe8-bf45460285f1">POLICY_DNS_DOMAIN_INFO</a> structure. 


### -field PolicyDnsDomainInformationInt


### -field PolicyLocalAccountDomainInformation


### -field PolicyLastEntry




## -see-also




<a href="https://msdn.microsoft.com/2d543500-f639-4ef7-91f4-cdc5060dd567">LsaQueryInformationPolicy</a>



<a href="https://msdn.microsoft.com/2aa3b09e-2cd9-4a09-bfd6-b37c97266dcb">LsaSetInformationPolicy</a>



<a href="https://msdn.microsoft.com/0e38ac5f-40db-405d-9394-b6bcb7c652b5">POLICY_ACCOUNT_DOMAIN_INFO</a>



<a href="https://msdn.microsoft.com/3442e5e5-78cf-4bda-ba11-0f51ee40df16">POLICY_AUDIT_EVENTS_INFO</a>



<a href="https://msdn.microsoft.com/5b2879cf-e0dc-4844-bfe8-bf45460285f1">POLICY_DNS_DOMAIN_INFO</a>



<a href="https://msdn.microsoft.com/f66abe33-d8c8-45b8-9b94-d6890d786aaa">POLICY_LSA_SERVER_ROLE_INFO</a>



<a href="https://msdn.microsoft.com/ef4d1d1d-9b1b-4d67-80b8-2b548ec31a87">POLICY_MODIFICATION_INFO</a>



<a href="https://msdn.microsoft.com/20102da1-bc05-4ea5-9a2d-a50ecba5fd88">POLICY_PRIMARY_DOMAIN_INFO</a>
 

 

