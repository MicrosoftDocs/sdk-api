---
UID: NS:ntsecapi._POLICY_PRIMARY_DOMAIN_INFO
title: POLICY_PRIMARY_DOMAIN_INFO (ntsecapi.h)
description: The PolicyPrimaryDomainInformation value and POLICY_PRIMARY_DOMAIN_INFO structure are obsolete. Use the PolicyDnsDomainInformation and POLICY_DNS_DOMAIN_INFO structure instead.
helpviewer_keywords: ["*PPOLICY_PRIMARY_DOMAIN_INFO","POLICY_PRIMARY_DOMAIN_INFO","POLICY_PRIMARY_DOMAIN_INFO structure [Security]","PPOLICY_PRIMARY_DOMAIN_INFO","PPOLICY_PRIMARY_DOMAIN_INFO structure pointer [Security]","_POLICY_PRIMARY_DOMAIN_INFO","_lsa_policy_primary_domain_info","ntsecapi/POLICY_PRIMARY_DOMAIN_INFO","ntsecapi/PPOLICY_PRIMARY_DOMAIN_INFO","security.policy_primary_domain_info"]
old-location: security\policy_primary_domain_info.htm
tech.root: security
ms.assetid: 20102da1-bc05-4ea5-9a2d-a50ecba5fd88
ms.date: 12/05/2018
ms.keywords: '*PPOLICY_PRIMARY_DOMAIN_INFO, POLICY_PRIMARY_DOMAIN_INFO, POLICY_PRIMARY_DOMAIN_INFO structure [Security], PPOLICY_PRIMARY_DOMAIN_INFO, PPOLICY_PRIMARY_DOMAIN_INFO structure pointer [Security], _POLICY_PRIMARY_DOMAIN_INFO, _lsa_policy_primary_domain_info, ntsecapi/POLICY_PRIMARY_DOMAIN_INFO, ntsecapi/PPOLICY_PRIMARY_DOMAIN_INFO, security.policy_primary_domain_info'
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
req.typenames: POLICY_PRIMARY_DOMAIN_INFO, *PPOLICY_PRIMARY_DOMAIN_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _POLICY_PRIMARY_DOMAIN_INFO
 - ntsecapi/_POLICY_PRIMARY_DOMAIN_INFO
 - PPOLICY_PRIMARY_DOMAIN_INFO
 - ntsecapi/PPOLICY_PRIMARY_DOMAIN_INFO
 - POLICY_PRIMARY_DOMAIN_INFO
 - ntsecapi/POLICY_PRIMARY_DOMAIN_INFO
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
 - POLICY_PRIMARY_DOMAIN_INFO
---

# POLICY_PRIMARY_DOMAIN_INFO structure


## -description

The <b>PolicyPrimaryDomainInformation</b> value and <b>POLICY_PRIMARY_DOMAIN_INFO</b> structure are obsolete. Use the <b>PolicyDnsDomainInformation</b> and 
<a href="/windows/desktop/api/lsalookup/ns-lsalookup-policy_dns_domain_info">POLICY_DNS_DOMAIN_INFO</a> structure instead.

## -struct-fields

### -field Name

An 
<a href="/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string">LSA_UNICODE_STRING</a> structure that specifies the name of the primary domain.

### -field Sid

Pointer to the SID of the primary domain.

## -see-also

<a href="/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string">LSA_UNICODE_STRING</a>



<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaqueryinformationpolicy">LsaQueryInformationPolicy</a>



<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsasetinformationpolicy">LsaSetInformationPolicy</a>



<a href="/windows/desktop/api/lsalookup/ns-lsalookup-policy_dns_domain_info">POLICY_DNS_DOMAIN_INFO</a>



<a href="/windows/desktop/api/ntsecapi/ne-ntsecapi-policy_information_class">POLICY_INFORMATION_CLASS</a>