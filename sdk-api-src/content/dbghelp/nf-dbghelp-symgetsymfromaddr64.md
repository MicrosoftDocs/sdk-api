---
UID: NF:dbghelp.SymGetSymFromAddr64
title: SymGetSymFromAddr64 function (dbghelp.h)
description: Locates the symbol for the specified address. (SymGetSymFromAddr64)
helpviewer_keywords: ["SymGetSymFromAddr","SymGetSymFromAddr function","SymGetSymFromAddr64","SymGetSymFromAddr64 function","_win32_symgetsymfromaddr64","base.symgetsymfromaddr64","dbghelp/SymGetSymFromAddr","dbghelp/SymGetSymFromAddr64"]
old-location: base\symgetsymfromaddr64.htm
tech.root: Debug
ms.assetid: c4882a3b-7773-4ab0-ad83-bdde512b5fb4
ms.date: 12/05/2018
ms.keywords: SymGetSymFromAddr, SymGetSymFromAddr function, SymGetSymFromAddr64, SymGetSymFromAddr64 function, _win32_symgetsymfromaddr64, base.symgetsymfromaddr64, dbghelp/SymGetSymFromAddr, dbghelp/SymGetSymFromAddr64
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
 - SymGetSymFromAddr64
 - dbghelp/SymGetSymFromAddr64
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Dbghelp.dll
api_name:
 - SymGetSymFromAddr64
 - SymGetSymFromAddr
---

## -description

Locates the symbol for the specified address.
<div class="alert"><b>Note</b>  This function is provided only for compatibility. Applications should use 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symfromaddr">SymFromAddr</a>.</div><div> </div>

## -parameters

### -param hProcess [in]

A handle to the process that was originally passed to the 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-syminitialize">SymInitialize</a> function.

### -param qwAddr [in]

The address for which a symbol is to be located. The address does not have to be on a symbol boundary. If the address comes after the beginning of a symbol and before the end of the symbol (the beginning of the symbol plus the symbol size), the symbol is found.

### -param pdwDisplacement [out, optional]

The displacement from the beginning of the symbol, or zero.

### -param Symbol [in, out]

A pointer to an 
<a href="/windows/desktop/api/dbghelp/ns-dbghelp-imagehlp_symbol">IMAGEHLP_SYMBOL64</a> structure.

## -returns

If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. To retrieve extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The 
<b>SymGetSymFromAddr64</b> function locates the symbol for a specified address. The modules are searched for the one the address belongs to. When the module is found, its symbol table is searched for a match. When the symbol is found, the symbol information is copied into the <i>Symbol</i> buffer provided by the caller. The caller must allocate the <i>Symbol</i> buffer properly and fill in the required parameters in the 
<a href="/windows/desktop/api/dbghelp/ns-dbghelp-imagehlp_symbol">IMAGEHLP_SYMBOL64</a> structure before calling 
<b>SymGetSymFromAddr64</b>.

All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

This function supersedes the <b>SymGetSymFromAddr</b> function. For more information, see 
<a href="/windows/desktop/Debug/updated-platform-support">Updated Platform Support</a>. <b>SymGetSymFromAddr</b> is defined as follows in Dbghelp.h. 


```cpp
#if !defined(_IMAGEHLP_SOURCE_) && defined(_IMAGEHLP64)
#define SymGetSymFromAddr SymGetSymFromAddr64
#else
BOOL
IMAGEAPI
SymGetSymFromAddr(
    __in HANDLE hProcess,
    __in DWORD dwAddr,
    __out_opt PDWORD pdwDisplacement,
    __inout PIMAGEHLP_SYMBOL Symbol
    );
#endif
```

## -see-also

<a href="/windows/desktop/Debug/dbghelp-functions">DbgHelp Functions</a>



<a href="/windows/desktop/api/dbghelp/ns-dbghelp-imagehlp_symbol">IMAGEHLP_SYMBOL64</a>



<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symfromaddr">SymFromAddr</a>



<a href="/windows/desktop/api/dbghelp/nf-dbghelp-syminitialize">SymInitialize</a>
