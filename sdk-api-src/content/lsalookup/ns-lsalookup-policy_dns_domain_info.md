---
UID: NS:lsalookup._POLICY_DNS_DOMAIN_INFO
title: POLICY_DNS_DOMAIN_INFO (lsalookup.h)
description: The POLICY_DNS_DOMAIN_INFO structure is used to set and query Domain Name System (DNS) information about the primary domain associated with a Policy object.
helpviewer_keywords: ["*PPOLICY_DNS_DOMAIN_INFO","POLICY_DNS_DOMAIN_INFO","POLICY_DNS_DOMAIN_INFO structure [Security]","PPOLICY_DNS_DOMAIN_INFO","PPOLICY_DNS_DOMAIN_INFO structure pointer [Security]","_lsa_policy_dns_domain_info","lsalookup/POLICY_DNS_DOMAIN_INFO","lsalookup/PPOLICY_DNS_DOMAIN_INFO","security.policy_dns_domain_info"]
old-location: security\policy_dns_domain_info.htm
tech.root: security
ms.assetid: 5b2879cf-e0dc-4844-bfe8-bf45460285f1
ms.date: 12/05/2018
ms.keywords: '*PPOLICY_DNS_DOMAIN_INFO, POLICY_DNS_DOMAIN_INFO, POLICY_DNS_DOMAIN_INFO structure [Security], PPOLICY_DNS_DOMAIN_INFO, PPOLICY_DNS_DOMAIN_INFO structure pointer [Security], _lsa_policy_dns_domain_info, lsalookup/POLICY_DNS_DOMAIN_INFO, lsalookup/PPOLICY_DNS_DOMAIN_INFO, security.policy_dns_domain_info'
req.header: lsalookup.h
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
req.typenames: POLICY_DNS_DOMAIN_INFO, *PPOLICY_DNS_DOMAIN_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _POLICY_DNS_DOMAIN_INFO
 - lsalookup/_POLICY_DNS_DOMAIN_INFO
 - PPOLICY_DNS_DOMAIN_INFO
 - lsalookup/PPOLICY_DNS_DOMAIN_INFO
 - POLICY_DNS_DOMAIN_INFO
 - lsalookup/POLICY_DNS_DOMAIN_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - LsaLookup.h
api_name:
 - POLICY_DNS_DOMAIN_INFO
---

# POLICY_DNS_DOMAIN_INFO structure


## -description

The <b>POLICY_DNS_DOMAIN_INFO</b> structure is used to set and query Domain Name System (DNS) information about the primary domain associated with a <a href="/windows/desktop/SecMgmt/policy-object">Policy</a> object. The 
<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaqueryinformationpolicy">LsaQueryInformationPolicy</a> and 
<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsasetinformationpolicy">LsaSetInformationPolicy</a> functions use this structure when their <i>InformationClass</i> parameters are set to <b>PolicyDnsDomainInformation</b>.

## -struct-fields

### -field Name

An 
<a href="/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string">LSA_UNICODE_STRING</a> structure that specifies the name of the primary domain. This is the same as the primary domain name in the 
<a href="/windows/desktop/api/ntsecapi/ns-ntsecapi-policy_primary_domain_info">POLICY_PRIMARY_DOMAIN_INFO</a> structure.

### -field DnsDomainName

An <a href="/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string">LSA_UNICODE_STRING</a> structure that specifies the DNS name of the primary domain.

### -field DnsForestName

An <a href="/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string">LSA_UNICODE_STRING</a> structure that specifies the DNS forest name of the primary domain. This is the DNS name of the domain at the root of the enterprise.

### -field DomainGuid

A 
<a href="/windows/win32/api/guiddef/ns-guiddef-guid">GUID</a> structure that contains the GUID of the primary domain.

### -field Sid

Pointer to the SID of the primary domain. This is the same as the primary domain SID in the <a href="/windows/desktop/api/ntsecapi/ns-ntsecapi-policy_primary_domain_info">POLICY_PRIMARY_DOMAIN_INFO</a> structure.

## -remarks

The <b>POLICY_DNS_DOMAIN_INFO</b> structure is an extended version of the 
<a href="/windows/desktop/api/ntsecapi/ns-ntsecapi-policy_primary_domain_info">POLICY_PRIMARY_DOMAIN_INFO</a> structure. Setting <b>POLICY_DNS_DOMAIN_INFO</b> information will overwrite the corresponding values in the <b>POLICY_PRIMARY_DOMAIN_INFO</b> (name and SID), and vice versa.

If the computer associated with the <a href="/windows/desktop/SecMgmt/policy-object">Policy</a> object is not a member of a domain, all structure members except <b>Name</b> are <b>NULL</b> or zero.

## -see-also

<a href="/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string">LSA_UNICODE_STRING</a>



<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaqueryinformationpolicy">LsaQueryInformationPolicy</a>



<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsasetinformationpolicy">LsaSetInformationPolicy</a>



<a href="/windows/desktop/api/ntsecapi/ne-ntsecapi-policy_information_class">POLICY_INFORMATION_CLASS</a>



<a href="/windows/desktop/api/ntsecapi/ns-ntsecapi-policy_primary_domain_info">POLICY_PRIMARY_DOMAIN_INFO</a>