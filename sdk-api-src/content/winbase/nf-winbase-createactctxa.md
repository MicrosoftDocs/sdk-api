---
UID: NF:winbase.CreateActCtxA
title: CreateActCtxA function
author: windows-driver-content
description: The CreateActCtx function creates an activation context.
old-location: setup\createactctx.htm
old-project: SbsCs
ms.assetid: 11508215-8d8b-4040-a725-88804103fac4
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: CreateActCtx, CreateActCtx function [Side-by-side Assemblies], CreateActCtxA, CreateActCtxW, _win32_createactctx, setup.createactctx, winbase/CreateActCtx, winbase/CreateActCtxA, winbase/CreateActCtxW
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
req.unicode-ansi: CreateActCtxW (Unicode) and CreateActCtxA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: PRIORITY_HINT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Kernel32.dll
-	API-MS-Win-Core-sidebyside-l1-1-0.dll
-	KernelBase.dll
-	API-Ms-Win-Core-Sidebyside-Ansi-L1-1-0.dll
-	Kernel32Legacy.dll
api_name:
-	CreateActCtx
-	CreateActCtxA
-	CreateActCtxW
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# CreateActCtxA function


## -description



			The 
<b>CreateActCtx</b> function creates an activation context. 
		


## -parameters




### -param pActCtx [in, out]

Pointer to an 
<a href="https://msdn.microsoft.com/b6f97f25-1834-44f7-86b7-33339481ba60">ACTCTX</a> structure that contains information about the activation context to be created.


## -returns



If the function succeeds, it returns a handle to the returned activation context. Otherwise, it returns INVALID_HANDLE_VALUE.

This function sets errors that can be retrieved by calling 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. For an example, see 
<a href="https://msdn.microsoft.com/4cc626ac-7574-44ce-8377-e0bdd8e74b7e">Retrieving the Last-Error Code</a>. For a complete list of error codes, see 
<a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">System Error Codes</a>.




## -remarks



Set any undefined bits in <b>dwFlags</b> of 
<a href="https://msdn.microsoft.com/b6f97f25-1834-44f7-86b7-33339481ba60">ACTCTX</a> to 0. If any undefined bits are not set to 0, the call to 
<b>CreateActCtx</b> that creates the activation context fails and returns an invalid parameter error code. The handle returned from 
<b>CreateActCtx</b> is passed in a call to 
<a href="https://msdn.microsoft.com/03381d95-1b5d-4b70-8c86-937ab9b2672d">ActivateActCtx</a> to activate the context for the current thread.




## -see-also




<a href="https://msdn.microsoft.com/b6f97f25-1834-44f7-86b7-33339481ba60">ACTCTX</a>
 

 

