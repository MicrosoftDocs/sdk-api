---
UID: NF:winbase.ZombifyActCtx
title: ZombifyActCtx function
author: windows-sdk-content
description: The ZombifyActCtx function deactivates the specified activation context, but does not deallocate it.
old-location: setup\zombifyactctx.htm
tech.root: SbsCs
ms.assetid: f421350a-66b5-4c5a-9e4c-ef69dbe39e7c
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ZombifyActCtx, ZombifyActCtx function [Side-by-side Assemblies], _win32_zombifyactctx, setup.zombifyactctx, winbase/ZombifyActCtx
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
 - ZombifyActCtx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- ZombifyActCtx
: 
---

# ZombifyActCtx function


## -description


The 
<b>ZombifyActCtx</b> function deactivates the specified activation context, but does not deallocate it.


## -parameters




### -param hActCtx [in]

Handle to the activation context that is to be deactivated.


## -returns



If the function succeeds, it returns <b>TRUE</b>. If a <b>null</b> handle is passed in the <i>hActCtx</i> parameter, NULL_INVALID_PARAMETER will be returned. Otherwise, it returns <b>FALSE</b>.

This function sets errors that can be retrieved by calling 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. For an example, see 
<a href="https://msdn.microsoft.com/4cc626ac-7574-44ce-8377-e0bdd8e74b7e">Retrieving the Last-Error Code</a>. For a complete list of error codes, see 
<a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">System Error Codes</a>.




## -remarks



This function is intended for use in debugging threads using activation contexts. If the activation context deactivated by this function is subsequently accessed, the access  fails and an assertion failure is shown in the debugger.




## -see-also




<a href="https://msdn.microsoft.com/b6f97f25-1834-44f7-86b7-33339481ba60">ACTCTX</a>
 

 

