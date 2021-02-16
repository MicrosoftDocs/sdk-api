---
UID: NS:ntsecpkg._SECPKG_DLL_FUNCTIONS
title: SECPKG_DLL_FUNCTIONS (ntsecpkg.h)
description: The SECPKG_DLL_FUNCTIONS structure contains pointers to the LSA functions that a security package can call while executing in-process with a client/server application.
helpviewer_keywords: ["*PSECPKG_DLL_FUNCTIONS","PSECPKG_DLL_FUNCTIONS","PSECPKG_DLL_FUNCTIONS structure pointer [Security]","SECPKG_DLL_FUNCTIONS","SECPKG_DLL_FUNCTIONS structure [Security]","_ssp_secpkg_dll_functions","ntsecpkg/PSECPKG_DLL_FUNCTIONS","ntsecpkg/SECPKG_DLL_FUNCTIONS","security.secpkg_dll_functions"]
old-location: security\secpkg_dll_functions.htm
tech.root: security
ms.assetid: a7881f06-792c-4791-9aa6-9a7eb202020b
ms.date: 12/05/2018
ms.keywords: '*PSECPKG_DLL_FUNCTIONS, PSECPKG_DLL_FUNCTIONS, PSECPKG_DLL_FUNCTIONS structure pointer [Security], SECPKG_DLL_FUNCTIONS, SECPKG_DLL_FUNCTIONS structure [Security], _ssp_secpkg_dll_functions, ntsecpkg/PSECPKG_DLL_FUNCTIONS, ntsecpkg/SECPKG_DLL_FUNCTIONS, security.secpkg_dll_functions'
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
req.typenames: SECPKG_DLL_FUNCTIONS, *PSECPKG_DLL_FUNCTIONS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SECPKG_DLL_FUNCTIONS
 - ntsecpkg/_SECPKG_DLL_FUNCTIONS
 - PSECPKG_DLL_FUNCTIONS
 - ntsecpkg/PSECPKG_DLL_FUNCTIONS
 - SECPKG_DLL_FUNCTIONS
 - ntsecpkg/SECPKG_DLL_FUNCTIONS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ntsecpkg.h
api_name:
 - SECPKG_DLL_FUNCTIONS
---

# SECPKG_DLL_FUNCTIONS structure


## -description

The <b>SECPKG_DLL_FUNCTIONS</b> structure contains pointers to the LSA functions that a <a href="/windows/desktop/SecGloss/s-gly">security package</a> can call while executing in-process with a client/server application. The <a href="/windows/desktop/SecGloss/l-gly">Local Security Authority</a> (LSA) provides this structure during user-mode initialization using each security package's 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spinstanceinitfn">SpInstanceInit</a> function.

## -struct-fields

### -field AllocateHeap

Pointer to the  <a href="/previous-versions/windows/desktop/legacy/aa374721(v=vs.85)">AllocateHeap</a> function.

### -field FreeHeap

Pointer to the  <a href="/previous-versions/windows/desktop/legacy/aa375418(v=vs.85)">FreeHeap</a> function.

### -field RegisterCallback

Pointer to the  <a href="/previous-versions/windows/desktop/legacy/aa379372(v=vs.85)">RegisterCallback</a> function.

### -field LocatePackageById