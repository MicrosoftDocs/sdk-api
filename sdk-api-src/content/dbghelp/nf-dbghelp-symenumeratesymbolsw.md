---
UID: NF:dbghelp.SymEnumerateSymbolsW
title: SymEnumerateSymbolsW function (dbghelp.h)
description: The SymEnumerateSymbolsW (Unicode) function enumerates all the symbols for a specified module.
helpviewer_keywords: ["SymEnumerateSymbols","SymEnumerateSymbols function","SymEnumerateSymbols64","SymEnumerateSymbols64 function","SymEnumerateSymbolsW","SymEnumerateSymbolsW64","_win32_symenumeratesymbols64","base.symenumeratesymbols64","dbghelp/SymEnumerateSymbols","dbghelp/SymEnumerateSymbols64","dbghelp/SymEnumerateSymbolsW","dbghelp/SymEnumerateSymbolsW64"]
old-location: base\symenumeratesymbols64.htm
tech.root: Debug
ms.assetid: f1aa710c-fbe5-4c9a-9956-5bd872b4b5be
ms.date: 08/04/2022
ms.keywords: SymEnumerateSymbols, SymEnumerateSymbols function, SymEnumerateSymbols64, SymEnumerateSymbols64 function, SymEnumerateSymbolsW, SymEnumerateSymbolsW64, _win32_symenumeratesymbols64, base.symenumeratesymbols64, dbghelp/SymEnumerateSymbols, dbghelp/SymEnumerateSymbols64, dbghelp/SymEnumerateSymbolsW, dbghelp/SymEnumerateSymbolsW64
req.header: dbghelp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SymEnumerateSymbolsW64 (Unicode) and SymEnumerateSymbols64 (ANSI)
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
 - SymEnumerateSymbolsW
 - dbghelp/SymEnumerateSymbolsW
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
 - SymEnumerateSymbols64
 - SymEnumerateSymbols64
 - SymEnumerateSymbolsW64
 - SymEnumerateSymbols
 - SymEnumerateSymbolsW
---

# SymEnumerateSymbolsW function


## -description

Enumerates all the symbols for a specified module.
<div class="alert"><b>Note</b>  This function is provided only for compatibility. Applications should use 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symenumsymbols">SymEnumSymbols</a>, which is faster and more powerful.</div><div> </div>

## -parameters

### -param hProcess [in]

A handle to the process. This handle must have been previously passed to the 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-syminitialize">SymInitialize</a> function.

### -param BaseOfDll [in]

The base address of the module for which symbols are to be enumerated.

### -param EnumSymbolsCallback [in]

The callback function that receives the symbol information. For more information, see 
<a href="/windows/desktop/api/dbghelp/nc-dbghelp-psym_enumsymbols_callback">SymEnumerateSymbolsProc64</a>.

### -param UserContext [in, optional]

A user-defined value or <b>NULL</b>. This value is passed to the callback function. Typically, this parameter is used by an application to pass a pointer to a data structure that enables the callback function establish some type of context.

## -returns

If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. To retrieve extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The 
<b>SymEnumerateSymbols64</b> function enumerates all the symbols for the specified module. The module information is located by the <i>BaseOfDll</i> parameter. The callback function is called once per symbol and is passed the information for each symbol.

All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

The Unicode version of this function, <b>SymEnumerateSymbolsW64</b> is defined as follows in Dbghelp.h. 


```cpp

BOOL
IMAGEAPI
SymEnumerateSymbolsW64(
    __in HANDLE hProcess,
    __in ULONG64 BaseOfDll,
    __in PSYM_ENUMSYMBOLS_CALLBACK64W EnumSymbolsCallback,
    __in_opt PVOID UserContext
    );
```


This function supersedes the <b>SymEnumerateSymbols</b> function. For more information, see 
<a href="/windows/desktop/Debug/updated-platform-support">Updated Platform Support</a>. <b>SymEnumerateSymbols</b> is defined as follows in Dbghelp.h. 


```cpp
#if !defined(_IMAGEHLP_SOURCE_) && defined(_IMAGEHLP64)
#define SymEnumerateSymbols SymEnumerateSymbols64
#define SymEnumerateSymbolsW SymEnumerateSymbolsW64
#else
BOOL
IMAGEAPI
SymEnumerateSymbols(
    __in HANDLE hProcess,
    __in ULONG BaseOfDll,
    __in PSYM_ENUMSYMBOLS_CALLBACK EnumSymbolsCallback,
    __in_opt PVOID UserContext
    );

BOOL
IMAGEAPI
SymEnumerateSymbolsW(
    __in HANDLE hProcess,
    __in ULONG BaseOfDll,
    __in PSYM_ENUMSYMBOLS_CALLBACKW EnumSymbolsCallback,
    __in_opt PVOID UserContext
    );
#endif
```

## -see-also

<a href="/windows/desktop/Debug/dbghelp-functions">DbgHelp Functions</a>



<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symenumsymbols">SymEnumSymbols</a>



<a href="/windows/desktop/api/dbghelp/nc-dbghelp-psym_enumsymbols_callback">SymEnumerateSymbolsProc64</a>



<a href="/windows/desktop/api/dbghelp/nf-dbghelp-syminitialize">SymInitialize</a>
