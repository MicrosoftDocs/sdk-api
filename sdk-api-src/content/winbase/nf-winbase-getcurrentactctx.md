---
UID: NF:winbase.GetCurrentActCtx
title: GetCurrentActCtx function
author: windows-sdk-content
description: The GetCurrentActCtx function returns the handle to the active activation context of the calling thread.
old-location: setup\getcurrentactctx.htm
tech.root: SbsCs
ms.assetid: d7603098-8d2d-4ace-9876-277b22f70ca8
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetCurrentActCtx, GetCurrentActCtx function [Side-by-side Assemblies], _win32_getcurrentactctx, setup.getcurrentactctx, winbase/GetCurrentActCtx
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winbase.h
req.include-header: Windows.h
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
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-sidebyside-l1-1-0.dll
 - KernelBase.dll
api_name:
 - GetCurrentActCtx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- GetCurrentActCtx
: 
---

# GetCurrentActCtx function


## -description


The 
<b>GetCurrentActCtx</b> function returns the handle to the active activation context of the calling thread.


## -parameters




### -param lphActCtx [out]

Pointer to the returned 
<a href="https://msdn.microsoft.com/b6f97f25-1834-44f7-86b7-33339481ba60">ACTCTX</a> structure that contains information on the active activation context.


## -returns



If the function succeeds, it returns <b>TRUE</b>. Otherwise, it returns <b>FALSE</b>.

This function sets errors that can be retrieved by calling 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. For an example, see 
<a href="https://msdn.microsoft.com/4cc626ac-7574-44ce-8377-e0bdd8e74b7e">Retrieving the Last-Error Code</a>. For a complete list of error codes, see 
<a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">System Error Codes</a>.




## -remarks



The calling thread is responsible for releasing the handle of the returned activation context. This function can return a null handle if no activation contexts have been activated by this thread. This is not an error.




## -see-also




<a href="https://msdn.microsoft.com/b6f97f25-1834-44f7-86b7-33339481ba60">ACTCTX</a>
 

 

