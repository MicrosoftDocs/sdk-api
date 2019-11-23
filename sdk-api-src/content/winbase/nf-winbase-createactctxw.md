---
UID: NF:winbase.CreateActCtxW
title: CreateActCtxW function (winbase.h)

description: The CreateActCtx function creates an activation context.
old-location: setup\createactctx.htm
tech.root: SbsCs
ms.assetid: 11508215-8d8b-4040-a725-88804103fac4

ms.date: 12/05/2018
ms.keywords: CreateActCtx, CreateActCtx function [Side-by-side Assemblies], CreateActCtxA, CreateActCtxW, _win32_createactctx, setup.createactctx, winbase/CreateActCtx, winbase/CreateActCtxA, winbase/CreateActCtxW
ms.topic: function
f1_keywords: 
 - "winbase/CreateActCtx"
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
req.unicode-ansi: CreateActCtxW (Unicode) and CreateActCtxA (ANSI)
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
 - API-Ms-Win-Core-Sidebyside-Ansi-L1-1-0.dll
 - Kernel32Legacy.dll
api_name:
 - CreateActCtx
 - CreateActCtxA
 - CreateActCtxW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CreateActCtxW function


## -description


The 
<b>CreateActCtx</b> function creates an activation context. 
		


## -parameters




### -param pActCtx [in, out]

Pointer to an 
<a href="https://docs.microsoft.com/windows/desktop/api/winbase/ns-winbase-actctxa">ACTCTX</a> structure that contains information about the activation context to be created.


## -returns



If the function succeeds, it returns a handle to the returned activation context. Otherwise, it returns INVALID_HANDLE_VALUE.

This function sets errors that can be retrieved by calling 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. For an example, see 
<a href="https://docs.microsoft.com/windows/desktop/Debug/retrieving-the-last-error-code">Retrieving the Last-Error Code</a>. For a complete list of error codes, see 
<a href="https://docs.microsoft.com/windows/desktop/Debug/system-error-codes">System Error Codes</a>.




## -remarks



Set any undefined bits in <b>dwFlags</b> of 
<a href="https://docs.microsoft.com/windows/desktop/api/winbase/ns-winbase-actctxa">ACTCTX</a> to 0. If any undefined bits are not set to 0, the call to 
<b>CreateActCtx</b> that creates the activation context fails and returns an invalid parameter error code. The handle returned from 
<b>CreateActCtx</b> is passed in a call to 
<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-activateactctx">ActivateActCtx</a> to activate the context for the current thread.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winbase/ns-winbase-actctxa">ACTCTX</a>
 

 

