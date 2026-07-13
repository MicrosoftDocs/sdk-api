---
UID: NF:dbghelp.SymUnloadModule
title: SymUnloadModule function (dbghelp.h)
description: Unloads the symbol table. (SymUnloadModule)
helpviewer_keywords: ["SymUnloadModule","SymUnloadModule function","SymUnloadModule64","SymUnloadModule64 function","_win32_symunloadmodule64","base.symunloadmodule64","dbghelp/SymUnloadModule","dbghelp/SymUnloadModule64"]
old-location: base\symunloadmodule64.htm
tech.root: Debug
ms.assetid: f4801039-eba2-4ec3-8c23-706ab89bb442
ms.date: 12/05/2018
ms.keywords: SymUnloadModule, SymUnloadModule function, SymUnloadModule64, SymUnloadModule64 function, _win32_symunloadmodule64, base.symunloadmodule64, dbghelp/SymUnloadModule, dbghelp/SymUnloadModule64
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
 - SymUnloadModule
 - dbghelp/SymUnloadModule
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
 - SymUnloadModule64
 - SymUnloadModule
---

# SymUnloadModule function


## -description

Unloads the symbol table.

## -parameters

### -param hProcess [in]

A handle to the process that was originally passed to the 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-syminitialize">SymInitialize</a> function.

### -param BaseOfDll [in]

The base address of the module that is to be unloaded.

## -returns

If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. To retrieve extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

The <a href="/windows/desktop/api/dbghelp/nf-dbghelp-symunloadmodule64">SymUnloadModule64</a> function supersedes this function. For more information, see 
<a href="/windows/desktop/Debug/updated-platform-support">Updated Platform Support</a>. <b>SymUnloadedModule</b> is defined as follows in Dbghelp.h. 


```cpp
#if !defined(_IMAGEHLP_SOURCE_) && defined(_IMAGEHLP64)
#define SymUnloadModule SymUnloadModule64
#else
BOOL
IMAGEAPI
SymUnloadModule(
    __in HANDLE hProcess,
    __in DWORD BaseOfDll
    );
#endif
```



#### Examples

For an example, see 
<a href="/windows/desktop/Debug/unloading-a-symbol-module">Unloading a Symbol Module</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/Debug/dbghelp-functions">DbgHelp Functions</a>



<a href="/windows/desktop/api/dbghelp/nf-dbghelp-syminitialize">SymInitialize</a>
