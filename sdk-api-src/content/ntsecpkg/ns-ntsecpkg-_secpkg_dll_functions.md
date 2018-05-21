---
UID: NS:ntsecpkg._SECPKG_DLL_FUNCTIONS
title: "_SECPKG_DLL_FUNCTIONS"
author: windows-driver-content
description: The SECPKG_DLL_FUNCTIONS structure contains pointers to the LSA functions that a security package can call while executing in-process with a client/server application.
old-location: security\secpkg_dll_functions.htm
old-project: SecAuthN
ms.assetid: a7881f06-792c-4791-9aa6-9a7eb202020b
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: "*PSECPKG_DLL_FUNCTIONS, PSECPKG_DLL_FUNCTIONS, PSECPKG_DLL_FUNCTIONS structure pointer [Security], SECPKG_DLL_FUNCTIONS, SECPKG_DLL_FUNCTIONS structure [Security], _SECPKG_DLL_FUNCTIONS, _ssp_secpkg_dll_functions, ntsecpkg/PSECPKG_DLL_FUNCTIONS, ntsecpkg/SECPKG_DLL_FUNCTIONS, security.secpkg_dll_functions"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
req.typenames: SECPKG_DLL_FUNCTIONS, *PSECPKG_DLL_FUNCTIONS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Ntsecpkg.h
api_name:
-	SECPKG_DLL_FUNCTIONS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# _SECPKG_DLL_FUNCTIONS structure


## -description


The <b>SECPKG_DLL_FUNCTIONS</b> structure contains pointers to the LSA functions that a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security package</a> can call while executing in-process with a client/server application. The <a href="https://msdn.microsoft.com/65dd9a04-fc7c-4179-95ff-dac7dad4668f">Local Security Authority</a> (LSA) provides this structure during user-mode initialization using each security package's 
<a href="https://msdn.microsoft.com/12f5903d-af13-40fd-8a23-2a28ffd9fc44">SpInstanceInit</a> function.


## -struct-fields




### -field AllocateHeap

Pointer to the  <a href="https://msdn.microsoft.com/8e97ea0e-42f5-4641-83d7-3858c533479c">AllocateHeap</a> function.
					


### -field FreeHeap

Pointer to the  <a href="https://msdn.microsoft.com/9aa28a2f-c71d-4f82-bc14-257ed51b9c88">FreeHeap</a> function.
					


### -field RegisterCallback

Pointer to the  <a href="https://msdn.microsoft.com/556f1fea-9675-4e2e-9fae-326e200cb98c">RegisterCallback</a> function.
					


### -field LocatePackageById

 



