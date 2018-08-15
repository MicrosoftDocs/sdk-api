---
UID: NF:winbase.ActivateActCtx
title: ActivateActCtx function
author: windows-sdk-content
description: The ActivateActCtx function activates the specified activation context.
old-location: setup\activateactctx.htm
old-project: sbscs
ms.assetid: 03381d95-1b5d-4b70-8c86-937ab9b2672d
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: ActivateActCtx, ActivateActCtx function [Side-by-side Assemblies], _win32_activateactctx, setup.activateactctx, winbase/ActivateActCtx
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winbase.h
req.include-header: Windows.h
req.redist: 
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
tech.root: 
req.typenames: PRIORITY_HINT
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
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ActivateActCtx function


## -description


The 
<b>ActivateActCtx</b> function activates the specified activation context. It does this by pushing the specified activation context to the top of the activation stack. The specified activation context is thus associated with the current thread and any appropriate side-by-side API functions.


## -parameters




### -param hActCtx [in]

Handle to an 
<a href="https://msdn.microsoft.com/b6f97f25-1834-44f7-86b7-33339481ba60">ACTCTX</a> structure that contains information on the activation context that is to be made active.


### -param lpCookie [out]

Pointer to a <b>ULONG_PTR</b> that functions as a cookie, uniquely identifying a specific, activated activation context.


## -returns



If the function succeeds, it returns <b>TRUE</b>. Otherwise, it returns <b>FALSE</b>.

This function sets errors that can be retrieved by calling 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. For an example, see 
<a href="https://msdn.microsoft.com/4cc626ac-7574-44ce-8377-e0bdd8e74b7e">Retrieving the Last-Error Code</a>. For a complete list of error codes, see 
<a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">System Error Codes</a>.




## -remarks



The <i>lpCookie</i> parameter is later passed to 
<a href="https://msdn.microsoft.com/2a53eb1a-ce0b-4b20-a346-1ff9636a74d6">DeactivateActCtx</a>, which verifies the pairing of calls to 
<b>ActivateActCtx</b> and 
<b>DeactivateActCtx</b> and ensures that the appropriate activation context is being deactivated. This is done because the deactivation of activation contexts must occur in the reverse order of activation.

The activation of activation contexts can be understood as pushing an activation context onto a stack of activation contexts. The activation context you activate through this function  redirects any binding to DLLs, window classes, COM servers, type libraries, and mutexes for any side-by-side APIs you call.

The top item of an activation context stack is the active, default-activation context of the current thread. If a null activation context handle is pushed onto the stack, thereby activating it, the default settings in the original manifest override all activation contexts that are lower on the stack.




## -see-also




<a href="https://msdn.microsoft.com/b6f97f25-1834-44f7-86b7-33339481ba60">ACTCTX</a>



<a href="https://msdn.microsoft.com/2a53eb1a-ce0b-4b20-a346-1ff9636a74d6">DeactivateActCtx</a>
 

 

