---
UID: NC:ntsecpkg.SpUserModeInitializeFn
title: SpUserModeInitializeFn
author: windows-driver-content
description: Called when a security support provider/authentication package (SSP/AP) DLL is loaded into the process space of a client/server application. This function provides the SECPKG_USER_FUNCTION_TABLE tables for each security package in the SSP/AP DLL.
old-location: security\spusermodeinitialize.htm
old-project: SecAuthN
ms.assetid: e260db29-995b-4f32-b389-4ef62b3b29bc
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: SpUserModeInitialize, SpUserModeInitialize function [Security], SpUserModeInitializeFn, _ssp_spusermodeinitialize, ntsecpkg/SpUserModeInitialize, security.spusermodeinitialize
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
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
req.typenames: TRUSTED_POSIX_OFFSET_INFO, *PTRUSTED_POSIX_OFFSET_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	Ntsecpkg.h
api_name:
-	SpUserModeInitialize
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# SpUserModeInitializeFn callback function


## -description


The <b>SpUserModeInitialize</b> function is called when a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security support provider</a>/<a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">authentication package</a> (SSP/AP) DLL is loaded into the process space of a client/server application. This function provides the 
<a href="https://msdn.microsoft.com/2b3fc6d1-2f55-4053-9271-f5cb5c318555">SECPKG_USER_FUNCTION_TABLE</a> tables for each <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security package</a> in the SSP/AP DLL.


## -parameters




### -param LsaVersion [in]

The version of the security provider DLL (either Secur32.dll or Security.dll).


### -param PackageVersion [out]

Pointer that returns the version of the SSP/AP DLL.


### -param *ppTables [out]

Pointer that returns an array of 
<a href="https://msdn.microsoft.com/2b3fc6d1-2f55-4053-9271-f5cb5c318555">SECPKG_USER_FUNCTION_TABLE</a> structures. Each structure is a table of pointers to the user-mode functions implemented by a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security package</a> deployed in the SSP/AP DLL.


### -param pcTables [out]

Pointer that returns the number of elements in the array pointed to by the <i>ppTables</i> parameter.


## -returns



If the function succeeds, return STATUS_SUCCESS.

If the function fails, return an <b>NTSTATUS</b> code that indicates the reason it failed.




## -remarks



The <b>SpUserModeInitialize</b> function must be implemented by SSP/AP DLLs that contain user-mode security packages.

The <i>ppTables</i> parameter should contain one 
<a href="https://msdn.microsoft.com/2b3fc6d1-2f55-4053-9271-f5cb5c318555">SECPKG_USER_FUNCTION_TABLE</a> for each user-mode security package deployed in the DLL. For more information on deploying security packages in DLLs, see 
<a href="https://msdn.microsoft.com/8f28177f-335a-4fa2-bf66-2ec1698bebec">User Mode Initialization</a>.




## -see-also




<a href="https://msdn.microsoft.com/2b3fc6d1-2f55-4053-9271-f5cb5c318555">SECPKG_USER_FUNCTION_TABLE</a>
 

 

