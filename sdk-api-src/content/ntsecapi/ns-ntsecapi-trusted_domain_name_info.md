---
UID: NS:ntsecapi._TRUSTED_DOMAIN_NAME_INFO
title: TRUSTED_DOMAIN_NAME_INFO (ntsecapi.h)
description: Used to query or set the name of a trusted domain.
helpviewer_keywords: ["*PTRUSTED_DOMAIN_NAME_INFO","PTRUSTED_DOMAIN_NAME_INFO","PTRUSTED_DOMAIN_NAME_INFO structure pointer [Security]","TRUSTED_DOMAIN_NAME_INFO","TRUSTED_DOMAIN_NAME_INFO structure [Security]","_TRUSTED_DOMAIN_NAME_INFO","_lsa_trusted_domain_name_info","ntsecapi/PTRUSTED_DOMAIN_NAME_INFO","ntsecapi/TRUSTED_DOMAIN_NAME_INFO","security.trusted_domain_name_info"]
old-location: security\trusted_domain_name_info.htm
tech.root: security
ms.assetid: 9bc1301b-1d09-4cd2-8590-e7756ee4792d
ms.date: 12/05/2018
ms.keywords: '*PTRUSTED_DOMAIN_NAME_INFO, PTRUSTED_DOMAIN_NAME_INFO, PTRUSTED_DOMAIN_NAME_INFO structure pointer [Security], TRUSTED_DOMAIN_NAME_INFO, TRUSTED_DOMAIN_NAME_INFO structure [Security], _TRUSTED_DOMAIN_NAME_INFO, _lsa_trusted_domain_name_info, ntsecapi/PTRUSTED_DOMAIN_NAME_INFO, ntsecapi/TRUSTED_DOMAIN_NAME_INFO, security.trusted_domain_name_info'
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
req.typenames: TRUSTED_DOMAIN_NAME_INFO, *PTRUSTED_DOMAIN_NAME_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _TRUSTED_DOMAIN_NAME_INFO
 - ntsecapi/_TRUSTED_DOMAIN_NAME_INFO
 - PTRUSTED_DOMAIN_NAME_INFO
 - ntsecapi/PTRUSTED_DOMAIN_NAME_INFO
 - TRUSTED_DOMAIN_NAME_INFO
 - ntsecapi/TRUSTED_DOMAIN_NAME_INFO
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
 - TRUSTED_DOMAIN_NAME_INFO
---

# TRUSTED_DOMAIN_NAME_INFO structure


## -description

The <b>TRUSTED_DOMAIN_NAME_INFO</b> structure is used to query or set the name of a trusted domain. The 
<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaquerytrusteddomaininfo">LsaQueryTrustedDomainInfo</a> and 
<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsasettrusteddomaininformation">LsaSetTrustedDomainInformation</a> functions use this structure when their <i>InformationClass</i> parameters are set to <b>TrustedDomainNameInformation</b>.

## -struct-fields

### -field Name

An 
<a href="/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string">LSA_UNICODE_STRING</a> structure that contains the name of a trusted domain.

## -see-also

<a href="/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string">LSA_UNICODE_STRING</a>



<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaquerytrusteddomaininfo">LsaQueryTrustedDomainInfo</a>



<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsasettrusteddomaininformation">LsaSetTrustedDomainInformation</a>



<a href="/windows/desktop/api/ntsecapi/ne-ntsecapi-trusted_information_class">TRUSTED_INFORMATION_CLASS</a>