---
UID: NS:ntsecapi._TRUSTED_DOMAIN_FULL_INFORMATION
title: TRUSTED_DOMAIN_FULL_INFORMATION (ntsecapi.h)
description: Used to retrieve complete information about a trusted domain.
helpviewer_keywords: ["*PTRUSTED_DOMAIN_FULL_INFORMATION","PTRUSTED_DOMAIN_FULL_INFORMATION","PTRUSTED_DOMAIN_FULL_INFORMATION structure pointer [Security]","TRUSTED_DOMAIN_FULL_INFORMATION","TRUSTED_DOMAIN_FULL_INFORMATION structure [Security]","_TRUSTED_DOMAIN_FULL_INFORMATION","_lsa_trusted_domain_full_information","ntsecapi/PTRUSTED_DOMAIN_FULL_INFORMATION","ntsecapi/TRUSTED_DOMAIN_FULL_INFORMATION","security.trusted_domain_full_information"]
old-location: security\trusted_domain_full_information.htm
tech.root: security
ms.assetid: b7abfe1e-d9e6-4583-a738-c16190ffd44d
ms.date: 12/05/2018
ms.keywords: '*PTRUSTED_DOMAIN_FULL_INFORMATION, PTRUSTED_DOMAIN_FULL_INFORMATION, PTRUSTED_DOMAIN_FULL_INFORMATION structure pointer [Security], TRUSTED_DOMAIN_FULL_INFORMATION, TRUSTED_DOMAIN_FULL_INFORMATION structure [Security], _TRUSTED_DOMAIN_FULL_INFORMATION, _lsa_trusted_domain_full_information, ntsecapi/PTRUSTED_DOMAIN_FULL_INFORMATION, ntsecapi/TRUSTED_DOMAIN_FULL_INFORMATION, security.trusted_domain_full_information'
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
req.typenames: TRUSTED_DOMAIN_FULL_INFORMATION, *PTRUSTED_DOMAIN_FULL_INFORMATION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _TRUSTED_DOMAIN_FULL_INFORMATION
 - ntsecapi/_TRUSTED_DOMAIN_FULL_INFORMATION
 - PTRUSTED_DOMAIN_FULL_INFORMATION
 - ntsecapi/PTRUSTED_DOMAIN_FULL_INFORMATION
 - TRUSTED_DOMAIN_FULL_INFORMATION
 - ntsecapi/TRUSTED_DOMAIN_FULL_INFORMATION
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
 - TRUSTED_DOMAIN_FULL_INFORMATION
---

# TRUSTED_DOMAIN_FULL_INFORMATION structure


## -description

The <b>TRUSTED_DOMAIN_FULL_INFORMATION</b> structure is used to retrieve complete information about a trusted domain. The 
<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaquerytrusteddomaininfo">LsaQueryTrustedDomainInfo</a> function uses this structure when its <i>InformationClass</i> parameter is set to <b>TrustedDomainFullInformation</b>.

## -struct-fields

### -field Information

A 
<a href="/windows/desktop/api/ntsecapi/ns-ntsecapi-trusted_domain_information_ex">TRUSTED_DOMAIN_INFORMATION_EX</a> structure containing extended information for a trusted domain.

### -field PosixOffset

A 
<a href="/windows/desktop/api/ntsecapi/ns-ntsecapi-trusted_posix_offset_info">TRUSTED_POSIX_OFFSET_INFO</a> structure containing the value used to generate Posix user and group identifiers for a trusted domain.

### -field AuthInformation

A 
<a href="/windows/desktop/api/ntsecapi/ns-ntsecapi-trusted_domain_auth_information">TRUSTED_DOMAIN_AUTH_INFORMATION</a> structure containing authentication information for a trusted domain.

## -see-also

<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaquerytrusteddomaininfo">LsaQueryTrustedDomainInfo</a>



<a href="/windows/desktop/api/ntsecapi/ns-ntsecapi-trusted_domain_auth_information">TRUSTED_DOMAIN_AUTH_INFORMATION</a>



<a href="/windows/desktop/api/ntsecapi/ns-ntsecapi-trusted_domain_information_ex">TRUSTED_DOMAIN_INFORMATION_EX</a>



<a href="/windows/desktop/api/ntsecapi/ne-ntsecapi-trusted_information_class">TRUSTED_INFORMATION_CLASS</a>



<a href="/windows/desktop/api/ntsecapi/ns-ntsecapi-trusted_posix_offset_info">TRUSTED_POSIX_OFFSET_INFO</a>