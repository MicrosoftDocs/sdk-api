---
UID: NC:ntsecpkg.SpGetInfoFn
title: SpGetInfoFn (ntsecpkg.h)
description: Provides general information about the security package, such as its name and capabilities.
helpviewer_keywords: ["SpGetInfo","SpGetInfo callback function [Security]","SpGetInfoFn","SpGetInfoFn callback","_ssp_spgetinfo","ntsecpkg/SpGetInfo","security.spgetinfo"]
old-location: security\spgetinfo.htm
tech.root: security
ms.assetid: e1e6f71f-6f54-424c-be49-7bc11cb19036
ms.date: 12/05/2018
ms.keywords: SpGetInfo, SpGetInfo callback function [Security], SpGetInfoFn, SpGetInfoFn callback, _ssp_spgetinfo, ntsecpkg/SpGetInfo, security.spgetinfo
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
 - SpGetInfoFn
 - ntsecpkg/SpGetInfoFn
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
 - SpGetInfo
---

# SpGetInfoFn callback function


## -description

The <b>SpGetInfo</b> function provides general information about the <a href="/windows/desktop/SecGloss/s-gly">security package</a>, such as its name and capabilities.

The <b>SpGetInfo</b> function is called when the client calls the 
<a href="/windows/desktop/api/sspi/nf-sspi-querysecuritypackageinfoa">QuerySecurityPackageInfo</a> function of the 
<a href="/windows/desktop/SecAuthN/sspi">Security Support Provider Interface</a>.

## -parameters

### -param PackageInfo [out]

Pointer to a 
<a href="/windows/desktop/api/sspi/ns-sspi-secpkginfoa">SecPkgInfo</a> structure that is allocated by the <a href="/windows/desktop/SecGloss/l-gly">Local Security Authority</a> (LSA) and must be populated by the package.

## -returns

If the function succeeds, return STATUS_SUCCESS.

If the function fails, return an <b>NTSTATUS</b> code that indicates the reason it failed.

## -remarks

It is safe to place pointers to constant or dynamic data into the 
<a href="/windows/desktop/api/sspi/ns-sspi-secpkginfoa">SecPkgInfo</a> structure—the LSA will make a copy of the data prior to forwarding it.

SSP/APs must implement the <b>SpGetInfo</b> function; however, the actual name given to the implementation is up to the developer.

A pointer to the <b>SpGetInfo</b> function is available in the 
<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-secpkg_function_table">SECPKG_FUNCTION_TABLE</a> structure received from the 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-splsamodeinitializefn">SpLsaModeInitialize</a> function.

## -see-also

<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-secpkg_function_table">SECPKG_FUNCTION_TABLE</a>



<a href="/windows/desktop/api/sspi/ns-sspi-secpkginfoa">SecPkgInfo</a>



<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-splsamodeinitializefn">SpLsaModeInitialize</a>