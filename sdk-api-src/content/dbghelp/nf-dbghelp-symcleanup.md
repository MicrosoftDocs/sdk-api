---
UID: NF:dbghelp.SymCleanup
title: SymCleanup function (dbghelp.h)
author: windows-sdk-content
description: Deallocates all resources associated with the process handle.
old-location: base\symcleanup.htm
tech.root: Debug
ms.assetid: 56107b71-a3f9-49af-9a90-df3585aed7c8
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: SymCleanup, SymCleanup function, _win32_symcleanup, base.symcleanup, dbghelp/SymCleanup
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
req.lib: Dbghelp.lib
req.dll: Dbghelp.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Dbghelp.dll
 - imagehlp.dll
api_name:
 - SymCleanup
product: Windows
targetos: Windows
req.typenames: 
req.redist: DbgHelp.dll 5.1 or later
ms.custom: 19H1
---

# SymCleanup function


## -description


Deallocates all resources associated with the process handle.


## -parameters




### -param hProcess [in]

A handle to the process that was originally passed to the 
<a href="https://docs.microsoft.com/windows/desktop/api/dbghelp/nf-dbghelp-syminitialize">SymInitialize</a> function.


## -returns



If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. To retrieve extended error information, call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



This function frees all resources associated with the process handle. Failure to call this function causes memory and resource leaks in the calling application

All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, call 
<a href="https://docs.microsoft.com/windows/desktop/api/dbghelp/nf-dbghelp-syminitialize">SymInitialize</a> only when your process starts and 
<b>SymCleanup</b> only when your process ends. It is not necessary for each thread in the process to call these functions.


#### Examples

For an example, see 
<a href="https://docs.microsoft.com/windows/desktop/Debug/terminating-the-symbol-handler">Terminating the Symbol Handler</a>.

<div class="code"></div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Debug/dbghelp-functions">DbgHelp Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dbghelp/nf-dbghelp-syminitialize">SymInitialize</a>
 

 

