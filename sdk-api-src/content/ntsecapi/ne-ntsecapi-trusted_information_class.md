---
UID: NE:ntsecapi._TRUSTED_INFORMATION_CLASS
title: TRUSTED_INFORMATION_CLASS (ntsecapi.h)
description: The TRUSTED_INFORMATION_CLASS enumeration type defines values that indicate the type of information to set or query for a trusted domain.
helpviewer_keywords: ["*PTRUSTED_INFORMATION_CLASS","PTRUSTED_INFORMATION_CLASS","PTRUSTED_INFORMATION_CLASS enumeration pointer [Security]","TRUSTED_INFORMATION_CLASS","TRUSTED_INFORMATION_CLASS enumeration [Security]","TrustedControllersInformation","TrustedDomainAuthInformation","TrustedDomainFullInformation","TrustedDomainInformationBasic","TrustedDomainInformationEx","TrustedDomainNameInformation","TrustedPasswordInformation","TrustedPosixOffsetInformation","_lsa_trusted_information_class","ntsecapi/PTRUSTED_INFORMATION_CLASS","ntsecapi/TRUSTED_INFORMATION_CLASS","ntsecapi/TrustedControllersInformation","ntsecapi/TrustedDomainAuthInformation","ntsecapi/TrustedDomainFullInformation","ntsecapi/TrustedDomainInformationBasic","ntsecapi/TrustedDomainInformationEx","ntsecapi/TrustedDomainNameInformation","ntsecapi/TrustedPasswordInformation","ntsecapi/TrustedPosixOffsetInformation","security.trusted_information_class"]
old-location: security\trusted_information_class.htm
tech.root: security
ms.assetid: 442a0944-b498-4d9f-b338-d5aed1663d8d
ms.date: 12/05/2018
ms.keywords: '*PTRUSTED_INFORMATION_CLASS, PTRUSTED_INFORMATION_CLASS, PTRUSTED_INFORMATION_CLASS enumeration pointer [Security], TRUSTED_INFORMATION_CLASS, TRUSTED_INFORMATION_CLASS enumeration [Security], TrustedControllersInformation, TrustedDomainAuthInformation, TrustedDomainFullInformation, TrustedDomainInformationBasic, TrustedDomainInformationEx, TrustedDomainNameInformation, TrustedPasswordInformation, TrustedPosixOffsetInformation, _lsa_trusted_information_class, ntsecapi/PTRUSTED_INFORMATION_CLASS, ntsecapi/TRUSTED_INFORMATION_CLASS, ntsecapi/TrustedControllersInformation, ntsecapi/TrustedDomainAuthInformation, ntsecapi/TrustedDomainFullInformation, ntsecapi/TrustedDomainInformationBasic, ntsecapi/TrustedDomainInformationEx, ntsecapi/TrustedDomainNameInformation, ntsecapi/TrustedPasswordInformation, ntsecapi/TrustedPosixOffsetInformation, security.trusted_information_class'
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
req.typenames: TRUSTED_INFORMATION_CLASS, *PTRUSTED_INFORMATION_CLASS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _TRUSTED_INFORMATION_CLASS
 - ntsecapi/_TRUSTED_INFORMATION_CLASS
 - PTRUSTED_INFORMATION_CLASS
 - ntsecapi/PTRUSTED_INFORMATION_CLASS
 - TRUSTED_INFORMATION_CLASS
 - ntsecapi/TRUSTED_INFORMATION_CLASS
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
 - TRUSTED_INFORMATION_CLASS
---

# TRUSTED_INFORMATION_CLASS enumeration


## -description

The <b>TRUSTED_INFORMATION_CLASS</b> enumeration type defines values that indicate the type of information to set or query for a trusted domain.

Each value has an associated structure that the 
<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaquerytrusteddomaininfo">LsaQueryTrustedDomainInfo</a> and 
<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsasettrusteddomaininformation">LsaSetTrustedDomainInformation</a> functions use to store the information.

## -enum-fields

### -field TrustedDomainNameInformation:1

Query or set the name of a trusted domain. Use the 
<a href="/windows/desktop/api/ntsecapi/ns-ntsecapi-trusted_domain_name_info">TRUSTED_DOMAIN_NAME_INFO</a> structure.

### -field TrustedControllersInformation

This value is obsolete.

### -field TrustedPosixOffsetInformation

Query or set the value used to generate Posix user and group identifiers. Use the 
<a href="/windows/desktop/api/ntsecapi/ns-ntsecapi-trusted_posix_offset_info">TRUSTED_POSIX_OFFSET_INFO</a> structure.

### -field TrustedPasswordInformation

This value has been superseded by the <b>TrustedDomainAuthInformation</b> value.

### -field TrustedDomainInformationBasic

This value is obsolete.

### -field TrustedDomainInformationEx

Query extended information for a trusted domain. Use the 
<a href="/windows/desktop/api/ntsecapi/ns-ntsecapi-trusted_domain_information_ex">TRUSTED_DOMAIN_INFORMATION_EX</a> structure.

### -field TrustedDomainAuthInformation

Query authentication information for a trusted domain. Use the 
<a href="/windows/desktop/api/ntsecapi/ns-ntsecapi-trusted_domain_auth_information">TRUSTED_DOMAIN_AUTH_INFORMATION</a> structure.

### -field TrustedDomainFullInformation

Query complete information for a trusted domain. This information includes the Posix offset information, authentication information, and the extended information returned for the <b>TrustedDomainInformationEx</b> value. Use the 
<a href="/windows/desktop/api/ntsecapi/ns-ntsecapi-trusted_domain_full_information">TRUSTED_DOMAIN_FULL_INFORMATION</a> structure.

### -field TrustedDomainAuthInformationInternal

### -field TrustedDomainFullInformationInternal

### -field TrustedDomainInformationEx2Internal

### -field TrustedDomainFullInformation2Internal

### -field TrustedDomainSupportedEncryptionTypes

## -see-also

<a href="/windows/desktop/api/lsalookup/ns-lsalookup-lsa_trust_information">LSA_TRUST_INFORMATION</a>



<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaquerytrusteddomaininfo">LsaQueryTrustedDomainInfo</a>



<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsasettrusteddomaininformation">LsaSetTrustedDomainInformation</a>



<a href="/windows/desktop/api/ntsecapi/ns-ntsecapi-trusted_domain_auth_information">TRUSTED_DOMAIN_AUTH_INFORMATION</a>



<a href="/windows/desktop/api/ntsecapi/ns-ntsecapi-trusted_domain_full_information">TRUSTED_DOMAIN_FULL_INFORMATION</a>



<a href="/windows/desktop/api/ntsecapi/ns-ntsecapi-trusted_domain_information_ex">TRUSTED_DOMAIN_INFORMATION_EX</a>



<a href="/windows/desktop/api/ntsecapi/ns-ntsecapi-trusted_domain_name_info">TRUSTED_DOMAIN_NAME_INFO</a>



<a href="/windows/desktop/api/ntsecapi/ns-ntsecapi-trusted_password_info">TRUSTED_PASSWORD_INFO</a>



<a href="/windows/desktop/api/ntsecapi/ns-ntsecapi-trusted_posix_offset_info">TRUSTED_POSIX_OFFSET_INFO</a>
