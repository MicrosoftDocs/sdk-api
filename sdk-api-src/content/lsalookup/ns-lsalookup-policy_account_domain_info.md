---
UID: NS:lsalookup._POLICY_ACCOUNT_DOMAIN_INFO
title: POLICY_ACCOUNT_DOMAIN_INFO (lsalookup.h)
description: Used to set and query the name and SID of the system's account domain.
helpviewer_keywords: ["*PPOLICY_ACCOUNT_DOMAIN_INFO","POLICY_ACCOUNT_DOMAIN_INFO","POLICY_ACCOUNT_DOMAIN_INFO structure [Security]","PPOLICY_ACCOUNT_DOMAIN_INFO","PPOLICY_ACCOUNT_DOMAIN_INFO structure pointer [Security]","_lsa_policy_account_domain_info","lsalookup/POLICY_ACCOUNT_DOMAIN_INFO","lsalookup/PPOLICY_ACCOUNT_DOMAIN_INFO","security.policy_account_domain_info"]
old-location: security\policy_account_domain_info.htm
tech.root: security
ms.assetid: 0e38ac5f-40db-405d-9394-b6bcb7c652b5
ms.date: 12/05/2018
ms.keywords: '*PPOLICY_ACCOUNT_DOMAIN_INFO, POLICY_ACCOUNT_DOMAIN_INFO, POLICY_ACCOUNT_DOMAIN_INFO structure [Security], PPOLICY_ACCOUNT_DOMAIN_INFO, PPOLICY_ACCOUNT_DOMAIN_INFO structure pointer [Security], _lsa_policy_account_domain_info, lsalookup/POLICY_ACCOUNT_DOMAIN_INFO, lsalookup/PPOLICY_ACCOUNT_DOMAIN_INFO, security.policy_account_domain_info'
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
req.typenames: POLICY_ACCOUNT_DOMAIN_INFO, *PPOLICY_ACCOUNT_DOMAIN_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _POLICY_ACCOUNT_DOMAIN_INFO
 - lsalookup/_POLICY_ACCOUNT_DOMAIN_INFO
 - PPOLICY_ACCOUNT_DOMAIN_INFO
 - lsalookup/PPOLICY_ACCOUNT_DOMAIN_INFO
 - POLICY_ACCOUNT_DOMAIN_INFO
 - lsalookup/POLICY_ACCOUNT_DOMAIN_INFO
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
 - POLICY_ACCOUNT_DOMAIN_INFO
---

# POLICY_ACCOUNT_DOMAIN_INFO structure


## -description

The <b>POLICY_ACCOUNT_DOMAIN_INFO</b> structure is used to set and query the name and SID of the system's account domain. The 
<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaqueryinformationpolicy">LsaQueryInformationPolicy</a> and 
<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsasetinformationpolicy">LsaSetInformationPolicy</a> functions use this structure when their <i>InformationClass</i> parameters are set to <b>PolicyAccountDomainInformation</b>.

## -struct-fields

### -field DomainName

An 
<a href="/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string">LSA_UNICODE_STRING</a> structure that specifies the name of the account domain.

### -field DomainSid

Pointer to the SID of the account domain.

## -see-also

<a href="/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string">LSA_UNICODE_STRING</a>



<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaqueryinformationpolicy">LsaQueryInformationPolicy</a>



<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsasetinformationpolicy">LsaSetInformationPolicy</a>



<a href="/windows/desktop/api/ntsecapi/ne-ntsecapi-policy_information_class">POLICY_INFORMATION_CLASS</a>