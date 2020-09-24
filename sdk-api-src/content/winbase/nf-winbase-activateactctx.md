---
UID: NF:winbase.ActivateActCtx
title: ActivateActCtx function (winbase.h)
description: The ActivateActCtx function activates the specified activation context.
helpviewer_keywords: ["ActivateActCtx","ActivateActCtx function [Side-by-side Assemblies]","_win32_activateactctx","setup.activateactctx","winbase/ActivateActCtx"]
old-location: setup\activateactctx.htm
tech.root: setup
ms.assetid: 03381d95-1b5d-4b70-8c86-937ab9b2672d
ms.date: 12/05/2018
ms.keywords: ActivateActCtx, ActivateActCtx function [Side-by-side Assemblies], _win32_activateactctx, setup.activateactctx, winbase/ActivateActCtx
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ActivateActCtx
 - winbase/ActivateActCtx
dev_langs:
 - c++
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
 - ActivateActCtx
---

# ActivateActCtx function


## -description

The 
<b>ActivateActCtx</b> function activates the specified activation context. It does this by pushing the specified activation context to the top of the activation stack. The specified activation context is thus associated with the current thread and any appropriate side-by-side API functions.

## -parameters

### -param hActCtx [in]

Handle to an 
<a href="/windows/desktop/api/winbase/ns-winbase-actctxa">ACTCTX</a> structure that contains information on the activation context that is to be made active.

### -param lpCookie [out]

Pointer to a <b>ULONG_PTR</b> that functions as a cookie, uniquely identifying a specific, activated activation context.

## -returns

If the function succeeds, it returns <b>TRUE</b>. Otherwise, it returns <b>FALSE</b>.

This function sets errors that can be retrieved by calling 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. For an example, see 
<a href="/windows/desktop/Debug/retrieving-the-last-error-code">Retrieving the Last-Error Code</a>. For a complete list of error codes, see 
<a href="/windows/desktop/Debug/system-error-codes">System Error Codes</a>.

## -remarks

The <i>lpCookie</i> parameter is later passed to 
<a href="/windows/desktop/api/winbase/nf-winbase-deactivateactctx">DeactivateActCtx</a>, which verifies the pairing of calls to 
<b>ActivateActCtx</b> and 
<b>DeactivateActCtx</b> and ensures that the appropriate activation context is being deactivated. This is done because the deactivation of activation contexts must occur in the reverse order of activation.

The activation of activation contexts can be understood as pushing an activation context onto a stack of activation contexts. The activation context you activate through this function  redirects any binding to DLLs, window classes, COM servers, type libraries, and mutexes for any side-by-side APIs you call.

The top item of an activation context stack is the active, default-activation context of the current thread. If a null activation context handle is pushed onto the stack, thereby activating it, the default settings in the original manifest override all activation contexts that are lower on the stack.

## -see-also

<a href="/windows/desktop/api/winbase/ns-winbase-actctxa">ACTCTX</a>



<a href="/windows/desktop/api/winbase/nf-winbase-deactivateactctx">DeactivateActCtx</a>