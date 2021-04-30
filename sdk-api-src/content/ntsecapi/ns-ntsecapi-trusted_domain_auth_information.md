---
UID: NS:ntsecapi._TRUSTED_DOMAIN_AUTH_INFORMATION
title: TRUSTED_DOMAIN_AUTH_INFORMATION (ntsecapi.h)
description: The TRUSTED_DOMAIN_AUTH_INFORMATION structure is used to retrieve authentication information for a trusted domain. The LsaQueryTrustedDomainInfo function uses this structure when its InformationClass parameter is set to TrustedDomainAuthInformation.
helpviewer_keywords: ["*PTRUSTED_DOMAIN_AUTH_INFORMATION","PTRUSTED_DOMAIN_AUTH_INFORMATION","PTRUSTED_DOMAIN_AUTH_INFORMATION structure pointer [Security]","TRUSTED_DOMAIN_AUTH_INFORMATION","TRUSTED_DOMAIN_AUTH_INFORMATION structure [Security]","_TRUSTED_DOMAIN_AUTH_INFORMATION","_lsa_trusted_domain_auth_information","ntsecapi/PTRUSTED_DOMAIN_AUTH_INFORMATION","ntsecapi/TRUSTED_DOMAIN_AUTH_INFORMATION","security.trusted_domain_auth_information"]
old-location: security\trusted_domain_auth_information.htm
tech.root: security
ms.assetid: 2ec606d7-42bd-47cc-a4cd-82908774aa43
ms.date: 12/05/2018
ms.keywords: '*PTRUSTED_DOMAIN_AUTH_INFORMATION, PTRUSTED_DOMAIN_AUTH_INFORMATION, PTRUSTED_DOMAIN_AUTH_INFORMATION structure pointer [Security], TRUSTED_DOMAIN_AUTH_INFORMATION, TRUSTED_DOMAIN_AUTH_INFORMATION structure [Security], _TRUSTED_DOMAIN_AUTH_INFORMATION, _lsa_trusted_domain_auth_information, ntsecapi/PTRUSTED_DOMAIN_AUTH_INFORMATION, ntsecapi/TRUSTED_DOMAIN_AUTH_INFORMATION, security.trusted_domain_auth_information'
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
req.typenames: TRUSTED_DOMAIN_AUTH_INFORMATION, *PTRUSTED_DOMAIN_AUTH_INFORMATION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _TRUSTED_DOMAIN_AUTH_INFORMATION
 - ntsecapi/_TRUSTED_DOMAIN_AUTH_INFORMATION
 - PTRUSTED_DOMAIN_AUTH_INFORMATION
 - ntsecapi/PTRUSTED_DOMAIN_AUTH_INFORMATION
 - TRUSTED_DOMAIN_AUTH_INFORMATION
 - ntsecapi/TRUSTED_DOMAIN_AUTH_INFORMATION
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
 - TRUSTED_DOMAIN_AUTH_INFORMATION
---

# TRUSTED_DOMAIN_AUTH_INFORMATION structure


## -description

The <b>TRUSTED_DOMAIN_AUTH_INFORMATION</b> structure is used to retrieve authentication information for a trusted domain. The 
<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaquerytrusteddomaininfo">LsaQueryTrustedDomainInfo</a> function uses this structure when its <i>InformationClass</i> parameter is set to <b>TrustedDomainAuthInformation</b>.

## -struct-fields

### -field IncomingAuthInfos

Specifies the number of entries in the <b>IncomingAuthenticationInformation</b> and <b>IncomingPreviousAuthenticationInformation</b> arrays.

### -field IncomingAuthenticationInformation

Pointer to an array of 
<a href="/windows/desktop/api/ntsecapi/ns-ntsecapi-lsa_auth_information">LSA_AUTH_INFORMATION</a> structures containing the authentication information for the incoming side of a trust relationship.

### -field IncomingPreviousAuthenticationInformation

Pointer to an array of <a href="/windows/desktop/api/ntsecapi/ns-ntsecapi-lsa_auth_information">LSA_AUTH_INFORMATION</a> structures containing the previous authentication information (or old password) for the incoming side of a trust relationship. There must be one of these for every entry in the <b>IncomingAuthenticationInformation</b> array.

### -field OutgoingAuthInfos

Specifies the number of entries in the <b>OutgoingAuthenticationInformation</b> and <b>OutgoingPreviousAuthenticationInformation</b> arrays.

### -field OutgoingAuthenticationInformation

Pointer to an array of <a href="/windows/desktop/api/ntsecapi/ns-ntsecapi-lsa_auth_information">LSA_AUTH_INFORMATION</a> structures containing the authentication information for the outgoing side of a trust relationship.

### -field OutgoingPreviousAuthenticationInformation

Pointer to an array of <a href="/windows/desktop/api/ntsecapi/ns-ntsecapi-lsa_auth_information">LSA_AUTH_INFORMATION</a> structures containing the previous authentication information (or old password) for the outgoing side of a trust relationship. There must be one of these for every entry in the <b>OutgoingAuthenticationInformation</b> array.

## -see-also

<a href="/windows/desktop/api/ntsecapi/ns-ntsecapi-lsa_auth_information">LSA_AUTH_INFORMATION</a>



<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsacreatetrusteddomainex">LsaCreateTrustedDomainEx</a>



<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaquerytrusteddomaininfo">LsaQueryTrustedDomainInfo</a>



<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaquerytrusteddomaininfobyname">LsaQueryTrustedDomainInfoByName</a>



<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsasettrusteddomaininfobyname">LsaSetTrustedDomainInfoByName</a>



<a href="/windows/desktop/api/ntsecapi/ne-ntsecapi-trusted_information_class">TRUSTED_INFORMATION_CLASS</a>