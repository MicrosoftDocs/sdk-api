---
UID: NF:dbghelp.SymCleanup
title: SymCleanup function (dbghelp.h)
description: Deallocates all resources associated with the process handle.
helpviewer_keywords: ["SymCleanup","SymCleanup function","_win32_symcleanup","base.symcleanup","dbghelp/SymCleanup"]
old-location: base\symcleanup.htm
tech.root: Debug
ms.assetid: 56107b71-a3f9-49af-9a90-df3585aed7c8
ms.date: 12/05/2018
ms.keywords: SymCleanup, SymCleanup function, _win32_symcleanup, base.symcleanup, dbghelp/SymCleanup
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
targetos: Windows
req.typenames: 
req.redist: DbgHelp.dll 5.1 or later
ms.custom: 19H1
f1_keywords:
 - SymCleanup
 - dbghelp/SymCleanup
dev_langs:
 - c++
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
---

# SymCleanup function


## -description

Deallocates all resources associated with the process handle.

## -parameters

### -param hProcess [in]

A handle to the process that was originally passed to the 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-syminitialize">SymInitialize</a> function.

## -returns

If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. To retrieve extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

This function frees all resources associated with the process handle. Failure to call this function causes memory and resource leaks in the calling application.

All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, call 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-syminitialize">SymInitialize</a> only when your process starts and 
<b>SymCleanup</b> only when your process ends. It is not necessary for each thread in the process to call these functions.


#### Examples

For an example, see 
<a href="/windows/desktop/Debug/terminating-the-symbol-handler">Terminating the Symbol Handler</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/Debug/dbghelp-functions">DbgHelp Functions</a>



<a href="/windows/desktop/api/dbghelp/nf-dbghelp-syminitialize">SymInitialize</a>
