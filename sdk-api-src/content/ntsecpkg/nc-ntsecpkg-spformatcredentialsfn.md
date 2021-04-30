---
UID: NC:ntsecpkg.SpFormatCredentialsFn
title: SpFormatCredentialsFn (ntsecpkg.h)
description: Formats credentials to be stored in a user object.
helpviewer_keywords: ["SpFormatCredentials","SpFormatCredentials callback function [Security]","SpFormatCredentialsFn","SpFormatCredentialsFn callback","_ssp_spformatcredentials","ntsecpkg/SpFormatCredentials","security.spformatcredentials"]
old-location: security\spformatcredentials.htm
tech.root: security
ms.assetid: c6036636-7f22-4f64-b507-59212d37638b
ms.date: 12/05/2018
ms.keywords: SpFormatCredentials, SpFormatCredentials callback function [Security], SpFormatCredentialsFn, SpFormatCredentialsFn callback, _ssp_spformatcredentials, ntsecpkg/SpFormatCredentials, security.spformatcredentials
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
 - SpFormatCredentialsFn
 - ntsecpkg/SpFormatCredentialsFn
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
 - SpFormatCredentials
---

# SpFormatCredentialsFn callback function


## -description

Formats <a href="/windows/desktop/SecGloss/c-gly">credentials</a> to be stored in a user object.

## -parameters

### -param Credentials [in]

Pointer to a 
<a href="/windows/desktop/api/sspi/ns-sspi-secbuffer">SecBuffer</a> structure containing the credentials to be formatted.

### -param FormattedCredentials [out]

Pointer to a <a href="/windows/desktop/api/sspi/ns-sspi-secbuffer">SecBuffer</a> structure containing the formatted credentials. Allocate memory for the structure using the 
<a href="/previous-versions/windows/desktop/legacy/aa374721(v=vs.85)">AllocateHeap</a> function.

## -returns

If the function succeeds, return STATUS_SUCCESS.

If the function fails, return an <b>NTSTATUS</b> code that indicates the reason it failed.

## -remarks

SSP/APs must implement the <b>SpFormatCredentials</b> function; however, the actual name given to the implementation is up to the developer.

A pointer to the <b>SpFormatCredentials</b> function is available in the 
<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-secpkg_user_function_table">SECPKG_USER_FUNCTION_TABLE</a> structure received from the 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spusermodeinitializefn">SpUserModeInitialize</a> function.

## -see-also

<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_allocate_lsa_heap">AllocateHeap</a>



<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-secpkg_user_function_table">SECPKG_USER_FUNCTION_TABLE</a>



<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spusermodeinitializefn">SpUserModeInitialize</a>