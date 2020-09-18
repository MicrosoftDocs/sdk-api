---
UID: NC:ntsecpkg.SpDeleteCredentialsFn
title: SpDeleteCredentialsFn (ntsecpkg.h)
description: Deletes credentials from a security package's list of primary or supplemental credentials.
helpviewer_keywords: ["SpDeleteCredentials","SpDeleteCredentials callback function [Security]","SpDeleteCredentialsFn","SpDeleteCredentialsFn callback","_ssp_spdeletecredentials","ntsecpkg/SpDeleteCredentials","security.spdeletecredentials"]
old-location: security\spdeletecredentials.htm
tech.root: security
ms.assetid: 14f41fc2-1e28-4ae5-9f2e-00f2500b7819
ms.date: 12/05/2018
ms.keywords: SpDeleteCredentials, SpDeleteCredentials callback function [Security], SpDeleteCredentialsFn, SpDeleteCredentialsFn callback, _ssp_spdeletecredentials, ntsecpkg/SpDeleteCredentials, security.spdeletecredentials
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
 - SpDeleteCredentialsFn
 - ntsecpkg/SpDeleteCredentialsFn
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
 - SpDeleteCredentials
---

# SpDeleteCredentialsFn callback function


## -description

Deletes <a href="/windows/desktop/SecGloss/c-gly">credentials</a> from a <a href="/windows/desktop/SecGloss/s-gly">security package's</a> list of <a href="/windows/desktop/SecGloss/p-gly">primary</a> or <a href="/windows/desktop/SecGloss/s-gly">supplemental</a> credentials.

## -parameters

### -param CredentialHandle [in]

A handle to the credentials to delete.

### -param Key [in]

Pointer to a 
<a href="/windows/desktop/api/sspi/ns-sspi-secbuffer">SecBuffer</a> structure whose contents indicate which credentials to delete. The information stored in the <i>Key</i> parameter is package specific.

## -returns

If the function succeeds, return STATUS_SUCCESS.

If the function fails, return an <b>NTSTATUS</b> code that indicates the reason it failed.

## -remarks

SSP/APs must implement the <b>SpDeleteCredentials</b> function; however, the actual name given to the implementation is up to the developer.

A pointer to the <b>SpDeleteCredentials</b> function is available in the 
<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-secpkg_function_table">SECPKG_FUNCTION_TABLE</a> structure received from the 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-splsamodeinitializefn">SpLsaModeInitialize</a> function.

## -see-also

<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-secpkg_function_table">SECPKG_FUNCTION_TABLE</a>



<a href="/windows/desktop/api/sspi/ns-sspi-secbuffer">SecBuffer</a>



<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-splsamodeinitializefn">SpLsaModeInitialize</a>