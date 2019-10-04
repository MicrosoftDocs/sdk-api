---
UID: NF:winbase.GetCurrentActCtx
title: GetCurrentActCtx function (winbase.h)
author: windows-sdk-content
description: The GetCurrentActCtx function returns the handle to the active activation context of the calling thread.
old-location: setup\getcurrentactctx.htm
tech.root: SbsCs
ms.assetid: d7603098-8d2d-4ace-9876-277b22f70ca8
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetCurrentActCtx, GetCurrentActCtx function [Side-by-side Assemblies], _win32_getcurrentactctx, setup.getcurrentactctx, winbase/GetCurrentActCtx
ms.topic: function
f1_keywords: 
 - "winbase/GetCurrentActCtx"
dev_langs:
 - c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GetCurrentActCtx function


## -description


The 
<b>GetCurrentActCtx</b> function returns the handle to the active activation context of the calling thread.


## -parameters




### -param lphActCtx [out]

Pointer to the returned 
<a href="https://docs.microsoft.com/windows/desktop/api/winbase/ns-winbase-actctxa">ACTCTX</a> structure that contains information on the active activation context.


## -returns



If the function succeeds, it returns <b>TRUE</b>. Otherwise, it returns <b>FALSE</b>.

This function sets errors that can be retrieved by calling 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. For an example, see 
<a href="https://docs.microsoft.com/windows/desktop/Debug/retrieving-the-last-error-code">Retrieving the Last-Error Code</a>. For a complete list of error codes, see 
<a href="https://docs.microsoft.com/windows/desktop/Debug/system-error-codes">System Error Codes</a>.




## -remarks



The calling thread is responsible for releasing the handle of the returned activation context. This function can return a null handle if no activation contexts have been activated by this thread. This is not an error.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winbase/ns-winbase-actctxa">ACTCTX</a>
 

 

