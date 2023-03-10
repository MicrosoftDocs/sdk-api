---
UID: NE:ntsecapi._POLICY_INFORMATION_CLASS
title: POLICY_INFORMATION_CLASS (ntsecapi.h)
description: Defines values that indicate the type of information to set or query in a Policy object.
helpviewer_keywords: ["*PPOLICY_INFORMATION_CLASS","POLICY_INFORMATION_CLASS","POLICY_INFORMATION_CLASS enumeration [Security]","PPOLICY_INFORMATION_CLASS","PPOLICY_INFORMATION_CLASS enumeration pointer [Security]","PolicyAccountDomainInformation","PolicyAuditEventsInformation","PolicyAuditFullQueryInformation","PolicyAuditFullSetInformation","PolicyAuditLogInformation","PolicyDefaultQuotaInformation","PolicyDnsDomainInformation","PolicyLsaServerRoleInformation","PolicyModificationInformation","PolicyPdAccountInformation","PolicyPrimaryDomainInformation","PolicyReplicaSourceInformation","_lsa_policy_information_class","ntsecapi/POLICY_INFORMATION_CLASS","ntsecapi/PPOLICY_INFORMATION_CLASS","ntsecapi/PolicyAccountDomainInformation","ntsecapi/PolicyAuditEventsInformation","ntsecapi/PolicyAuditFullQueryInformation","ntsecapi/PolicyAuditFullSetInformation","ntsecapi/PolicyAuditLogInformation","ntsecapi/PolicyDefaultQuotaInformation","ntsecapi/PolicyDnsDomainInformation","ntsecapi/PolicyLsaServerRoleInformation","ntsecapi/PolicyModificationInformation","ntsecapi/PolicyPdAccountInformation","ntsecapi/PolicyPrimaryDomainInformation","ntsecapi/PolicyReplicaSourceInformation","security.policy_information_class"]
old-location: security\policy_information_class.htm
tech.root: security
ms.assetid: b734b5e8-1ee9-436b-b2a9-210ae79fbaf5
ms.date: 12/05/2018
ms.keywords: '*PPOLICY_INFORMATION_CLASS, POLICY_INFORMATION_CLASS, POLICY_INFORMATION_CLASS enumeration [Security], PPOLICY_INFORMATION_CLASS, PPOLICY_INFORMATION_CLASS enumeration pointer [Security], PolicyAccountDomainInformation, PolicyAuditEventsInformation, PolicyAuditFullQueryInformation, PolicyAuditFullSetInformation, PolicyAuditLogInformation, PolicyDefaultQuotaInformation, PolicyDnsDomainInformation, PolicyLsaServerRoleInformation, PolicyModificationInformation, PolicyPdAccountInformation, PolicyPrimaryDomainInformation, PolicyReplicaSourceInformation, _lsa_policy_information_class, ntsecapi/POLICY_INFORMATION_CLASS, ntsecapi/PPOLICY_INFORMATION_CLASS, ntsecapi/PolicyAccountDomainInformation, ntsecapi/PolicyAuditEventsInformation, ntsecapi/PolicyAuditFullQueryInformation, ntsecapi/PolicyAuditFullSetInformation, ntsecapi/PolicyAuditLogInformation, ntsecapi/PolicyDefaultQuotaInformation, ntsecapi/PolicyDnsDomainInformation, ntsecapi/PolicyLsaServerRoleInformation, ntsecapi/PolicyModificationInformation, ntsecapi/PolicyPdAccountInformation, ntsecapi/PolicyPrimaryDomainInformation, ntsecapi/PolicyReplicaSourceInformation, security.policy_information_class'
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
targetos: Windows
req.typenames: POLICY_INFORMATION_CLASS, *PPOLICY_INFORMATION_CLASS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _POLICY_INFORMATION_CLASS
 - ntsecapi/_POLICY_INFORMATION_CLASS
 - PPOLICY_INFORMATION_CLASS
 - ntsecapi/PPOLICY_INFORMATION_CLASS
 - POLICY_INFORMATION_CLASS
 - ntsecapi/POLICY_INFORMATION_CLASS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ntsecapi.h
api_name:
 - POLICY_INFORMATION_CLASS
---

# POLICY_INFORMATION_CLASS enumeration


## -description

The <b>POLICY_INFORMATION_CLASS</b> enumeration  defines values that indicate the type of information to set or query in a <a href="/windows/desktop/SecMgmt/policy-object">Policy</a> object.

## -enum-fields

### -field PolicyAuditLogInformation:1

This value is obsolete.

### -field PolicyAuditEventsInformation

Query or set the auditing rules of the system. You can enable or disable auditing and specify the types of events that are audited. Use the 
<a href="/windows/desktop/api/ntsecapi/ns-ntsecapi-policy_audit_events_info">POLICY_AUDIT_EVENTS_INFO</a> structure.

### -field PolicyPrimaryDomainInformation

This value is obsolete. Use the <b>PolicyDnsDomainInformation</b> value instead.

### -field PolicyPdAccountInformation

This value is obsolete.

### -field PolicyAccountDomainInformation

Query or set the name and SID of the account domain of the system. Use the 
<a href="/windows/desktop/api/lsalookup/ns-lsalookup-policy_account_domain_info">POLICY_ACCOUNT_DOMAIN_INFO</a> structure.

### -field PolicyLsaServerRoleInformation

Query or set the role of an LSA server. Use the 
<a href="/windows/desktop/api/ntsecapi/ns-ntsecapi-policy_lsa_server_role_info">POLICY_LSA_SERVER_ROLE_INFO</a> structure.

### -field PolicyReplicaSourceInformation

This value is obsolete.

### -field PolicyDefaultQuotaInformation

This value is obsolete.

### -field PolicyModificationInformation

Query or set information about the creation time and last modification of the LSA database. Use the 
<a href="/windows/desktop/api/ntsecapi/ns-ntsecapi-policy_modification_info">POLICY_MODIFICATION_INFO</a> structure.

### -field PolicyAuditFullSetInformation

This value is obsolete.

### -field PolicyAuditFullQueryInformation

This value is obsolete.

### -field PolicyDnsDomainInformation

Query or set Domain Name System (DNS) information about the account domain associated with a <a href="/windows/desktop/SecMgmt/policy-object">Policy</a> object. Use the 
<a href="/windows/desktop/api/lsalookup/ns-lsalookup-policy_dns_domain_info">POLICY_DNS_DOMAIN_INFO</a> structure.

### -field PolicyDnsDomainInformationInt

### -field PolicyLocalAccountDomainInformation

### -field PolicyMachineAccountInformation

### -field PolicyLastEntry

## -see-also

<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaqueryinformationpolicy">LsaQueryInformationPolicy</a>



<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsasetinformationpolicy">LsaSetInformationPolicy</a>



<a href="/windows/desktop/api/lsalookup/ns-lsalookup-policy_account_domain_info">POLICY_ACCOUNT_DOMAIN_INFO</a>



<a href="/windows/desktop/api/ntsecapi/ns-ntsecapi-policy_audit_events_info">POLICY_AUDIT_EVENTS_INFO</a>



<a href="/windows/desktop/api/lsalookup/ns-lsalookup-policy_dns_domain_info">POLICY_DNS_DOMAIN_INFO</a>



<a href="/windows/desktop/api/ntsecapi/ns-ntsecapi-policy_lsa_server_role_info">POLICY_LSA_SERVER_ROLE_INFO</a>



<a href="/windows/desktop/api/ntsecapi/ns-ntsecapi-policy_modification_info">POLICY_MODIFICATION_INFO</a>



<a href="/windows/desktop/api/ntsecapi/ns-ntsecapi-policy_primary_domain_info">POLICY_PRIMARY_DOMAIN_INFO</a>
