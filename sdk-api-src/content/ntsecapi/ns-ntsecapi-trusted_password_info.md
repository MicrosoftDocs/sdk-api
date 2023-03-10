---
UID: NS:ntsecapi._TRUSTED_PASSWORD_INFO
title: TRUSTED_PASSWORD_INFO (ntsecapi.h)
description: The TRUSTED_PASSWORD_INFO structure is used to query or set the password for a trusted domain.
helpviewer_keywords: ["*PTRUSTED_PASSWORD_INFO","PTRUSTED_PASSWORD_INFO","PTRUSTED_PASSWORD_INFO structure pointer [Security]","TRUSTED_PASSWORD_INFO","TRUSTED_PASSWORD_INFO structure [Security]","_TRUSTED_PASSWORD_INFO","_lsa_trusted_password_info","ntsecapi/PTRUSTED_PASSWORD_INFO","ntsecapi/TRUSTED_PASSWORD_INFO","security.trusted_password_info"]
old-location: security\trusted_password_info.htm
tech.root: security
ms.assetid: 2c3aca10-8efd-4278-8127-2d31db776c0e
ms.date: 12/05/2018
ms.keywords: '*PTRUSTED_PASSWORD_INFO, PTRUSTED_PASSWORD_INFO, PTRUSTED_PASSWORD_INFO structure pointer [Security], TRUSTED_PASSWORD_INFO, TRUSTED_PASSWORD_INFO structure [Security], _TRUSTED_PASSWORD_INFO, _lsa_trusted_password_info, ntsecapi/PTRUSTED_PASSWORD_INFO, ntsecapi/TRUSTED_PASSWORD_INFO, security.trusted_password_info'
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
req.typenames: TRUSTED_PASSWORD_INFO, *PTRUSTED_PASSWORD_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _TRUSTED_PASSWORD_INFO
 - ntsecapi/_TRUSTED_PASSWORD_INFO
 - PTRUSTED_PASSWORD_INFO
 - ntsecapi/PTRUSTED_PASSWORD_INFO
 - TRUSTED_PASSWORD_INFO
 - ntsecapi/TRUSTED_PASSWORD_INFO
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
 - TRUSTED_PASSWORD_INFO
---

# TRUSTED_PASSWORD_INFO structure


## -description

The <b>TRUSTED_PASSWORD_INFO</b> structure is used to query or set the password for a trusted domain. The 
<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaquerytrusteddomaininfo">LsaQueryTrustedDomainInfo</a> and 
<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsasettrusteddomaininformation">LsaSetTrustedDomainInformation</a> functions use this structure when their <i>InformationClass</i> parameters are set to TrustedPasswordInformation.

## -struct-fields

### -field Password

An 
<a href="/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string">LSA_UNICODE_STRING</a> structure that contains the password to use when creating an authenticated connection to the domain.

### -field OldPassword

An <a href="/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string">LSA_UNICODE_STRING</a> structure that contains the old password. On set operations, if the <b>Buffer</b> member of this structure is <b>NULL</b>, the old password is set to the current password.

## -remarks

When you have finished using the <b>TRUSTED_PASSWORD_INFO</b> structure, clear the sensitive information from memory by calling the <a href="/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)">SecureZeroMemory</a> function. For more information about protecting passwords, see <a href="/windows/desktop/SecBP/handling-passwords">Handling Passwords</a>.

## -see-also

<a href="/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string">LSA_UNICODE_STRING</a>



<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaquerytrusteddomaininfo">LsaQueryTrustedDomainInfo</a>



<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsasettrusteddomaininformation">LsaSetTrustedDomainInformation</a>



<a href="/windows/desktop/api/ntsecapi/ne-ntsecapi-trusted_information_class">TRUSTED_INFORMATION_CLASS</a>