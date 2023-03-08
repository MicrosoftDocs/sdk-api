---
UID: NC:ntsecpkg.CredFreeCredentialsFn
title: CredFreeCredentialsFn (ntsecpkg.h)
description: Frees memory used to store credentials used by a security package.
helpviewer_keywords: ["CredFreeCredentialsFn","CredFreeCredentialsFn callback","CrediFreeCredentials","CrediFreeCredentials callback function [Security]","ntsecpkg/CrediFreeCredentials","security.credifreecredentials"]
old-location: security\credifreecredentials.htm
tech.root: security
ms.assetid: 9da22201-884d-4822-a769-c2ce0d36ec73
ms.date: 12/05/2018
ms.keywords: CredFreeCredentialsFn, CredFreeCredentialsFn callback, CrediFreeCredentials, CrediFreeCredentials callback function [Security], ntsecpkg/CrediFreeCredentials, security.credifreecredentials
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
 - CredFreeCredentialsFn
 - ntsecpkg/CredFreeCredentialsFn
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
 - CrediFreeCredentials
---

# CredFreeCredentialsFn callback function


## -description

Frees memory used to store credentials used by a  <a href="/windows/desktop/SecGloss/s-gly">security package</a>.

## -parameters

### -param Count [in]

The number of elements in the <i>Credentials</i> array.

### -param Credentials [in, out]

A pointer to a pointer that, on input, points to an array of  <a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-encrypted_credentialw">ENCRYPTED_CREDENTIALW</a> structures to be freed.

## -returns

If the function succeeds, the return value is STATUS_SUCCESS.
						

If the function fails, the return value is an NTSTATUS code that indicates the reason it failed.

## -remarks

A pointer to the <b>CrediFreeCredentials</b> function is available in the 
<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-lsa_secpkg_function_table">LSA_SECPKG_FUNCTION_TABLE</a> structure received by the 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spinitializefn">SpInitialize</a> function.

## -see-also

<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spinitializefn">SpInitialize</a>
