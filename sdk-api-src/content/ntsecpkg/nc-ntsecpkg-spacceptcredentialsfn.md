---
UID: NC:ntsecpkg.SpAcceptCredentialsFn
title: SpAcceptCredentialsFn (ntsecpkg.h)
description: Called by the Local Security Authority (LSA) to pass the security package any credentials stored for the authenticated security principal.
helpviewer_keywords: ["SpAcceptCredentials","SpAcceptCredentials callback function [Security]","SpAcceptCredentialsFn","SpAcceptCredentialsFn callback","_ssp_spacceptcredentials","ntsecpkg/SpAcceptCredentials","security.spacceptcredentials"]
old-location: security\spacceptcredentials.htm
tech.root: security
ms.assetid: bb382937-e5d6-452b-b166-505d0c80412c
ms.date: 12/05/2018
ms.keywords: SpAcceptCredentials, SpAcceptCredentials callback function [Security], SpAcceptCredentialsFn, SpAcceptCredentialsFn callback, _ssp_spacceptcredentials, ntsecpkg/SpAcceptCredentials, security.spacceptcredentials
req.header: ntsecpkg.h
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SpAcceptCredentialsFn
 - ntsecpkg/SpAcceptCredentialsFn
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Ntsecpkg.h
api_name:
 - SpAcceptCredentials
---

# SpAcceptCredentialsFn callback function


## -description

Called by the <a href="/windows/desktop/SecGloss/l-gly">Local Security Authority</a> (LSA) to pass the <a href="/windows/desktop/SecGloss/s-gly">security package</a> any <a href="/windows/desktop/SecGloss/c-gly">credentials</a> stored for the authenticated <a href="/windows/desktop/SecGloss/s-gly">security principal</a>. This function is called once for each set of credentials stored by the LSA.

## -parameters

### -param LogonType [in]

A 
<a href="/windows/desktop/api/ntsecapi/ne-ntsecapi-security_logon_type">SECURITY_LOGON_TYPE</a> value indicating the type of logon.

### -param AccountName [in]

Pointer to a 
<a href="/windows/desktop/api/subauth/ns-subauth-unicode_string">UNICODE_STRING</a> structure specifying the name of the logged-on account.

### -param PrimaryCredentials [in]

Pointer to a 
<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-secpkg_primary_cred">SECPKG_PRIMARY_CRED</a> structure containing the credentials used to logon. This structure can have <b>NULL</b> members.

### -param SupplementalCredentials [in]

Pointer to a 
<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-secpkg_supplemental_cred">SECPKG_SUPPLEMENTAL_CRED</a> structure containing package-specific <a href="/windows/desktop/SecGloss/s-gly">supplemental credentials</a>.

## -returns

If the function succeeds, return STATUS_SUCCESS.

If the function fails, return an <b>NTSTATUS</b> code that indicates the reason it failed.

## -remarks

The <a href="/windows/desktop/SecGloss/s-gly">security package</a> should save the credentials so that it can service requests for credentials. For additional information, see the 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spacquirecredentialshandlefn">SpAcquireCredentialsHandle</a> function.

SSP/APs must implement the <b>SpAcceptCredentials</b> function; unlike other SSP/AP functions the name of the function must be <b>SpAcceptCredentials</b>.

The LSA accesses the <b>SpAcceptCredentials</b> function through the 
<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-secpkg_function_table">SECPKG_FUNCTION_TABLE</a> structure received from the 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-splsamodeinitializefn">SpLsaModeInitialize</a> function.

## -see-also

<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-secpkg_primary_cred">SECPKG_PRIMARY_CRED</a>



<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-secpkg_supplemental_cred">SECPKG_SUPPLEMENTAL_CRED</a>



<a href="/windows/desktop/api/ntsecapi/ne-ntsecapi-security_logon_type">SECURITY_LOGON_TYPE</a>



<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spacquirecredentialshandlefn">SpAcquireCredentialsHandle</a>



<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-splsamodeinitializefn">SpLsaModeInitialize</a>