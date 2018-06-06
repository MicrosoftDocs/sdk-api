---
UID: NF:winbase.AddRefActCtx
title: AddRefActCtx function
author: windows-sdk-content
description: The AddRefActCtx function increments the reference count of the specified activation context.
old-location: setup\addrefactctx.htm
old-project: SbsCs
ms.assetid: 6812a3f4-53e4-4b60-be04-711ab4c37d12
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: AddRefActCtx, AddRefActCtx function [Side-by-side Assemblies], _win32_addrefactctx, setup.addrefactctx, winbase/AddRefActCtx
ms.prod: windows
ms.technology: windows-sdk
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
 - AddRefActCtx
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# AddRefActCtx function


## -description


The 
<b>AddRefActCtx</b> function increments the reference count of the specified activation context.


## -parameters




### -param hActCtx [in]

Handle to an 
<a href="https://msdn.microsoft.com/b6f97f25-1834-44f7-86b7-33339481ba60">ACTCTX</a> structure that contains information on the activation context for which the reference count is to be incremented.


## -returns



This function does not return a value.




## -remarks



This function is provided so that multiple clients can access a single activation context.




## -see-also




<a href="https://msdn.microsoft.com/b6f97f25-1834-44f7-86b7-33339481ba60">ACTCTX</a>
 

 

