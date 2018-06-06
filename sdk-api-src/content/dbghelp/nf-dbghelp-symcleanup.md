---
UID: NF:dbghelp.SymCleanup
title: SymCleanup function
author: windows-sdk-content
description: Deallocates all resources associated with the process handle.
old-location: base\symcleanup.htm
old-project: Debug
ms.assetid: 56107b71-a3f9-49af-9a90-df3585aed7c8
ms.author: windowssdkdev
ms.date: 05/17/2018
ms.keywords: SymCleanup, SymCleanup function, _win32_symcleanup, base.symcleanup, dbghelp/SymCleanup
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: dbghelp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.typenames: IMAGEHLP_SYMBOL_TYPE_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Dbghelp.dll
api_name:
 - SymCleanup
product: Windows
targetos: Windows
req.lib: Dbghelp.lib
req.dll: Dbghelp.dll
req.irql: 
---

# SymCleanup function


## -description


Deallocates all resources associated with the process handle.


## -parameters




### -param hProcess [in]

A handle to the process that was originally passed to the 
<a href="https://msdn.microsoft.com/fb1c98cb-6cd0-4218-aea4-384c24c66395">SymInitialize</a> function.


## -returns



If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. To retrieve extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



This function frees all resources associated with the process handle. Failure to call this function causes memory and resource leaks in the calling application

All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, call 
<a href="https://msdn.microsoft.com/fb1c98cb-6cd0-4218-aea4-384c24c66395">SymInitialize</a> only when your process starts and 
<b>SymCleanup</b> only when your process ends. It is not necessary for each thread in the process to call these functions.


#### Examples

For an example, see 
<a href="https://msdn.microsoft.com/270a1984-9e66-4dd2-accb-d715287f1ec0">Terminating the Symbol Handler</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/7b28f70b-2d97-4cc2-8064-dfb806f9cffa">DbgHelp Functions</a>



<a href="https://msdn.microsoft.com/fb1c98cb-6cd0-4218-aea4-384c24c66395">SymInitialize</a>
 

 

