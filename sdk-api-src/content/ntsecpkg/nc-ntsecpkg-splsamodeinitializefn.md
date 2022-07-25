---
UID: NC:ntsecpkg.SpLsaModeInitializeFn
title: SpLsaModeInitializeFn (ntsecpkg.h)
description: Provides the LSA with pointers to the functions implemented by each security package in the SSP/AP DLL.
helpviewer_keywords: ["SpLsaModeInitialize","SpLsaModeInitialize callback function [Security]","SpLsaModeInitializeFn","SpLsaModeInitializeFn callback","_ssp_splsamodeinitialize","ntsecpkg/SpLsaModeInitialize","security.splsamodeinitialize"]
old-location: security\splsamodeinitialize.htm
tech.root: security
ms.assetid: 1ef3770b-197f-4d5b-9933-b7f6f63e5627
ms.date: 12/05/2018
ms.keywords: SpLsaModeInitialize, SpLsaModeInitialize callback function [Security], SpLsaModeInitializeFn, SpLsaModeInitializeFn callback, _ssp_splsamodeinitialize, ntsecpkg/SpLsaModeInitialize, security.splsamodeinitialize
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
 - SpLsaModeInitializeFn
 - ntsecpkg/SpLsaModeInitializeFn
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
 - SpLsaModeInitialize
---

# SpLsaModeInitializeFn callback function


## -description

The <b>SpLsaModeInitialize</b> function is called once by the <a href="/windows/desktop/SecGloss/l-gly">Local Security Authority</a> (LSA) for each registered <a href="/windows/desktop/SecGloss/s-gly">security support provider</a>/<a href="/windows/desktop/SecGloss/a-gly">authentication package</a> (SSP/AP) DLL it loads. This function provides the LSA with pointers to the functions implemented by each <a href="/windows/desktop/SecGloss/s-gly">security package</a> in the SSP/AP DLL.

## -parameters

### -param LsaVersion [in]

The version of the LSA.

### -param PackageVersion [out]

Pointer to a <b>ULONG</b> that returns the SSP/AP DLL version number.

### -param ppTables [out]

Pointer to an array of 
<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-secpkg_function_table">SECPKG_FUNCTION_TABLE</a> structures. Each structure is a table of pointers to the functions implemented by a security package deployed in the SSP/AP DLL.

### -param pcTables [out]

Pointer that returns the number of elements in the array pointed to by the <i>ppTables</i> parameter.

## -returns

If the function succeeds, return STATUS_SUCCESS.

If the function fails, return an <b>NTSTATUS</b> code that indicates the reason it failed.

## -remarks

The <b>SpLsaModeInitialize</b> function must be implemented by SSP/AP DLLs.

The <i>ppTables</i> parameter should contain one 
<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-secpkg_function_table">SECPKG_FUNCTION_TABLE</a> for each security package deployed in the DLL.

## -see-also

<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-secpkg_function_table">SECPKG_FUNCTION_TABLE</a>
