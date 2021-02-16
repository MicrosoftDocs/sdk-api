---
UID: NC:ntsecpkg.SpInitializeFn
title: SpInitializeFn (ntsecpkg.h)
description: Is called once by the Local Security Authority (LSA) to provide a security package with general security information and a dispatch table of support functions.
helpviewer_keywords: ["SpInitialize","SpInitialize callback function [Security]","SpInitializeFn","SpInitializeFn callback","_ssp_spinitialize","ntsecpkg/SpInitialize","security.spinitialize"]
old-location: security\spinitialize.htm
tech.root: security
ms.assetid: d93bafc6-d946-4214-b3c0-5e5a8e359638
ms.date: 12/05/2018
ms.keywords: SpInitialize, SpInitialize callback function [Security], SpInitializeFn, SpInitializeFn callback, _ssp_spinitialize, ntsecpkg/SpInitialize, security.spinitialize
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
 - SpInitializeFn
 - ntsecpkg/SpInitializeFn
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
 - SpInitialize
---

# SpInitializeFn callback function


## -description

The <b>SpInitialize</b> function is called once by the <a href="/windows/desktop/SecGloss/l-gly">Local Security Authority</a> (LSA) to provide a <a href="/windows/desktop/SecGloss/s-gly">security package</a> with general security information and a dispatch table of support functions. The security package should save the information and do internal initialization processing, if any is needed.

## -parameters

### -param PackageId [in]

A unique identifier the LSA assigns to each security package. The value is valid until the system is restarted.

### -param Parameters [in]

A pointer to a 
<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-secpkg_parameters">SECPKG_PARAMETERS</a> structure containing primary domain and machine state information.

### -param FunctionTable [in]

Pointer to a table of LSA support functions that a security package can call.

## -returns

If the function succeeds, return STATUS_SUCCESS, or an informational status code.

If the function fails, return an NTSTATUS error code indicating the reason it failed. For more information, see Remarks.

## -remarks

If <b>SpInitialize</b> returns an NTSTATUS error code to the LSA, the package will be unloaded, and the <a href="/windows/desktop/SecGloss/l-gly">Local Security Authority</a> (LSA) will not include it in the list of available security packages.

SSP/APs must implement the <b>SpInitialize</b> function; however, the actual name given to the implementation is up to the developer.

A pointer to the SSP/AP's implementation of the <b>SpInitialize</b> function must be in the 
<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-secpkg_function_table">SECPKG_FUNCTION_TABLE</a> structure passed to the LSA from the 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-splsamodeinitializefn">SpLsaModeInitialize</a> function.

## -see-also

<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-secpkg_function_table">SECPKG_FUNCTION_TABLE</a>



<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-secpkg_parameters">SECPKG_PARAMETERS</a>



<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-splsamodeinitializefn">SpLsaModeInitialize</a>