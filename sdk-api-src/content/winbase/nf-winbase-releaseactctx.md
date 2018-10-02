---
UID: NF:winbase.ReleaseActCtx
title: ReleaseActCtx function
author: windows-sdk-content
description: The ReleaseActCtx function decrements the reference count of the specified activation context.
old-location: setup\releaseactctx.htm
tech.root: SbsCs
ms.assetid: aaf58969-06b7-4981-83af-651252339186
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ReleaseActCtx, ReleaseActCtx function [Side-by-side Assemblies], _win32_releaseactctx, setup.releaseactctx, winbase/ReleaseActCtx
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
 - ReleaseActCtx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ReleaseActCtx function


## -description


The 
<b>ReleaseActCtx</b> function decrements the reference count of the specified activation context.


## -parameters




### -param hActCtx [in]

Handle to the 
<a href="https://msdn.microsoft.com/b6f97f25-1834-44f7-86b7-33339481ba60">ACTCTX</a> structure that contains information on the activation context for which the reference count is to be decremented.


## -returns



This function does not return a value. On successful completion, the activation context reference count is decremented. The recipient of the reference-counted object must decrement the reference count when the object is no longer required.




## -remarks



When the reference count of an activation context becomes zero, the activation context structure is deallocated. Activation contexts have not been implemented as kernel objects, therefore, kernel handler functions cannot be used for activation contexts.

If the value of the <i>hActCtx</i> parameter is a null handle, this function does nothing and no error condition occurs.




## -see-also




<a href="https://msdn.microsoft.com/b6f97f25-1834-44f7-86b7-33339481ba60">ACTCTX</a>



<a href="https://msdn.microsoft.com/6812a3f4-53e4-4b60-be04-711ab4c37d12">AddRefActCtx</a>
 

 

