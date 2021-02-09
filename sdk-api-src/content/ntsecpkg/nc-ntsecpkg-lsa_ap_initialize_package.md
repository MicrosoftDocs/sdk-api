---
UID: NC:ntsecpkg.LSA_AP_INITIALIZE_PACKAGE
title: LSA_AP_INITIALIZE_PACKAGE (ntsecpkg.h)
description: Called once by the Local Security Authority (LSA) during system initialization to provide the authentication package a chance to initialize itself.
helpviewer_keywords: ["LSA_AP_INITIALIZE_PACKAGE","LSA_AP_INITIALIZE_PACKAGE callback","LsaApInitializePackage","LsaApInitializePackage callback function [Security]","_lsa_lsaapinitializepackage","ntsecpkg/LsaApInitializePackage","security.lsaapinitializepackage"]
old-location: security\lsaapinitializepackage.htm
tech.root: security
ms.assetid: 1fed5a5e-5dc1-4b59-aa28-bd1395a27742
ms.date: 12/05/2018
ms.keywords: LSA_AP_INITIALIZE_PACKAGE, LSA_AP_INITIALIZE_PACKAGE callback, LsaApInitializePackage, LsaApInitializePackage callback function [Security], _lsa_lsaapinitializepackage, ntsecpkg/LsaApInitializePackage, security.lsaapinitializepackage
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
 - LSA_AP_INITIALIZE_PACKAGE
 - ntsecpkg/LSA_AP_INITIALIZE_PACKAGE
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
 - LsaApInitializePackage
---

# LSA_AP_INITIALIZE_PACKAGE callback function


## -description

Called once by the <a href="/windows/desktop/SecGloss/l-gly">Local Security Authority</a> (LSA) during system initialization to provide the authentication package a chance to initialize itself.

## -parameters

### -param AuthenticationPackageId [in]

The identifier the LSA has assigned to the authentication package.

### -param LsaDispatchTable [in]

Pointer to an 
<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-lsa_dispatch_table">LSA_DISPATCH_TABLE</a> structure that contains the addresses of LSA functions that can be called by authentication packages. Your custom authentication package should save this information if it requires any of the functions described in 
<a href="/windows/desktop/SecAuthN/authentication-functions">LSA Functions Called by Authentication Packages</a>.

### -param Database [in, optional]

This parameter is not used; it is <b>NULL</b>.

### -param Confidentiality [in, optional]

This parameter is not used; it is <b>NULL</b>.

### -param AuthenticationPackageName [out]

Pointer to a pointer to an <a href="/windows/desktop/api/lsalookup/ns-lsalookup-lsa_string">LSA_STRING</a> structure that receives the name of the authentication package. The authentication package is responsible for allocating the structure and the buffer that contains this string (using the 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_allocate_lsa_heap">AllocateLsaHeap</a> function) and returning the address of the structure in this parameter. The buffer will be freed by the LSA when it is no longer needed.

## -returns

If the function succeeds, return STATUS_SUCCESS.

If the function fails, return an NTSTATUS error code. For more information, see 
<a href="/windows/desktop/SecMgmt/management-return-values">LSA Policy Function Return Values</a>.

## -remarks

This function must be implemented by authentication packages.

## -see-also

<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_allocate_lsa_heap">AllocateLsaHeap</a>
