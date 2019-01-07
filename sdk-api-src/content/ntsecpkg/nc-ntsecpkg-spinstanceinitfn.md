---
UID: NC:ntsecpkg.SpInstanceInitFn
title: SpInstanceInitFn
author: windows-sdk-content
description: Initializes user-mode security packages in an SSP/AP.
old-location: security\spinstanceinit.htm
tech.root: SecAuthN
ms.assetid: 12f5903d-af13-40fd-8a23-2a28ffd9fc44
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: SpInstanceInit, SpInstanceInit callback function [Security], SpInstanceInitFn, SpInstanceInitFn callback, _ssp_spinstanceinit, ntsecpkg/SpInstanceInit, security.spinstanceinit
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Ntsecpkg.h
api_name:
 - SpInstanceInit
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SpInstanceInitFn callback function


## -description


The <b>SpInstanceInit</b> function is called once for each <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security package</a> contained in an SSP/AP, when the SSP/AP is loaded into a client/server process. Security packages should use this function to perform any user mode-specific initialization.


## -parameters




### -param Version [in]

The version of the <a href="https://msdn.microsoft.com/65dd9a04-fc7c-4179-95ff-dac7dad4668f">Local Security Authority</a> (LSA).


### -param FunctionTable [in]

Pointer to a 
<a href="https://msdn.microsoft.com/a7881f06-792c-4791-9aa6-9a7eb202020b">SECPKG_DLL_FUNCTIONS</a> structure containing the support functions that the security package can use in user-mode.


### -param *UserFunctions [out]

This parameter is not used.


## -returns



If the function succeeds, return STATUS_SUCCESS.

If the function fails, return an <b>NTSTATUS</b> code that indicates the reason it failed.




## -remarks



The <b>SpInstanceInit</b> function is called once when the SSP/AP is loaded into the user-mode process, after the 
<a href="https://msdn.microsoft.com/e260db29-995b-4f32-b389-4ef62b3b29bc">SpUserModeInitialize</a> function is called.

SSP/APs must implement the <b>SpInstanceInit</b> function; however, the actual name given to the implementation is up to the developer.

A pointer to the <b>SpInstanceInit</b> function is available in the 
<a href="https://msdn.microsoft.com/2b3fc6d1-2f55-4053-9271-f5cb5c318555">SECPKG_USER_FUNCTION_TABLE</a> structure received from the <a href="https://msdn.microsoft.com/e260db29-995b-4f32-b389-4ef62b3b29bc">SpUserModeInitialize</a> function.




## -see-also




<a href="https://msdn.microsoft.com/2b3fc6d1-2f55-4053-9271-f5cb5c318555">SECPKG_USER_FUNCTION_TABLE</a>



<a href="https://msdn.microsoft.com/e260db29-995b-4f32-b389-4ef62b3b29bc">SpUserModeInitialize</a>
 

 

