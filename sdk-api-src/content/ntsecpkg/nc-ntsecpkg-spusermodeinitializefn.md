---
UID: NC:ntsecpkg.SpUserModeInitializeFn
title: SpUserModeInitializeFn (ntsecpkg.h)
description: Called when a security support provider/authentication package (SSP/AP) DLL is loaded into the process space of a client/server application. This function provides the SECPKG_USER_FUNCTION_TABLE tables for each security package in the SSP/AP DLL.
helpviewer_keywords: ["SpUserModeInitialize","SpUserModeInitialize callback function [Security]","SpUserModeInitializeFn","SpUserModeInitializeFn callback","_ssp_spusermodeinitialize","ntsecpkg/SpUserModeInitialize","security.spusermodeinitialize"]
old-location: security\spusermodeinitialize.htm
tech.root: security
ms.assetid: e260db29-995b-4f32-b389-4ef62b3b29bc
ms.date: 12/05/2018
ms.keywords: SpUserModeInitialize, SpUserModeInitialize callback function [Security], SpUserModeInitializeFn, SpUserModeInitializeFn callback, _ssp_spusermodeinitialize, ntsecpkg/SpUserModeInitialize, security.spusermodeinitialize
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
 - SpUserModeInitializeFn
 - ntsecpkg/SpUserModeInitializeFn
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
 - SpUserModeInitialize
---

# SpUserModeInitializeFn callback function


## -description

The <b>SpUserModeInitialize</b> function is called when a <a href="/windows/desktop/SecGloss/s-gly">security support provider</a>/<a href="/windows/desktop/SecGloss/a-gly">authentication package</a> (SSP/AP) DLL is loaded into the process space of a client/server application. This function provides the 
<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-secpkg_user_function_table">SECPKG_USER_FUNCTION_TABLE</a> tables for each <a href="/windows/desktop/SecGloss/s-gly">security package</a> in the SSP/AP DLL.

## -parameters

### -param LsaVersion [in]

The version of the security provider DLL (either Secur32.dll or Security.dll).

### -param PackageVersion [out]

Pointer that returns the version of the SSP/AP DLL.

### -param ppTables [out]

Pointer that returns an array of 
<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-secpkg_user_function_table">SECPKG_USER_FUNCTION_TABLE</a> structures. Each structure is a table of pointers to the user-mode functions implemented by a <a href="/windows/desktop/SecGloss/s-gly">security package</a> deployed in the SSP/AP DLL.

### -param pcTables [out]

Pointer that returns the number of elements in the array pointed to by the <i>ppTables</i> parameter.

## -returns

If the function succeeds, return STATUS_SUCCESS.

If the function fails, return an <b>NTSTATUS</b> code that indicates the reason it failed.

## -remarks

The <b>SpUserModeInitialize</b> function must be implemented by SSP/AP DLLs that contain user-mode security packages.

The <i>ppTables</i> parameter should contain one 
<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-secpkg_user_function_table">SECPKG_USER_FUNCTION_TABLE</a> for each user-mode security package deployed in the DLL. For more information on deploying security packages in DLLs, see 
<a href="/windows/desktop/SecAuthN/user-mode-initialization">User Mode Initialization</a>.

## -see-also

<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-secpkg_user_function_table">SECPKG_USER_FUNCTION_TABLE</a>
