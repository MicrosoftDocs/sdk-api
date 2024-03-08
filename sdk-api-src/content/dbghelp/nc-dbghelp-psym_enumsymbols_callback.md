---
UID: NC:dbghelp.PSYM_ENUMSYMBOLS_CALLBACK
title: PSYM_ENUMSYMBOLS_CALLBACK (dbghelp.h)
description: PSYM_ENUMSYMBOLS_CALLBACK (dbghelp.h) is an application-defined callback function used with the SymEnumerateSymbols64 function.
helpviewer_keywords: ["PSYM_ENUMSYMBOLS_CALLBACK","PSYM_ENUMSYMBOLS_CALLBACK64","PSYM_ENUMSYMBOLS_CALLBACK64W","SymEnumerateSymbolsProc64","SymEnumerateSymbolsProc64 callback","SymEnumerateSymbolsProc64 callback function","_win32_symenumeratesymbolsproc64","base.symenumeratesymbolsproc64","dbghelp/SymEnumerateSymbolsProc64"]
old-location: base\symenumeratesymbolsproc64.htm
tech.root: Debug
ms.assetid: e1430398-041f-4edd-b7b0-de3a60a42b37
ms.date: 08/03/2022
ms.keywords: PSYM_ENUMSYMBOLS_CALLBACK, PSYM_ENUMSYMBOLS_CALLBACK64, PSYM_ENUMSYMBOLS_CALLBACK64W, SymEnumerateSymbolsProc64, SymEnumerateSymbolsProc64 callback, SymEnumerateSymbolsProc64 callback function, _win32_symenumeratesymbolsproc64, base.symenumeratesymbolsproc64, dbghelp/SymEnumerateSymbolsProc64
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: DbgHelp.dll 5.1 or later
ms.custom: 19H1
f1_keywords:
 - PSYM_ENUMSYMBOLS_CALLBACK
 - dbghelp/PSYM_ENUMSYMBOLS_CALLBACK
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - DbgHelp.h
api_name:
 - SymEnumerateSymbolsProc64
---

# PSYM_ENUMSYMBOLS_CALLBACK callback function


## -description

An application-defined callback function used with the 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symenumeratesymbols">SymEnumerateSymbols64</a> function. It is called once for each enumerated symbol, and receives the symbol information.

The <b>PSYM_ENUMSYMBOLS_CALLBACK64</b> and <b>PSYM_ENUMSYMBOLS_CALLBACK64W</b> types define a pointer to this callback function. 
<b>SymEnumerateSymbolsProc64</b> is a placeholder for the application-defined function name.
<div class="alert"><b>Note</b>  This function is provided only for compatibility. Applications should use 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symenumsymbols">SymEnumSymbols</a>.</div><div> </div>

## -parameters

### -param SymbolName [in]

The name of the symbol. The name can be undecorated if the SYMOPT_UNDNAME option is used with the 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symsetoptions">SymSetOptions</a> function.

### -param SymbolAddress [in]

The virtual address for the beginning of the symbol.

### -param SymbolSize [in]

The size of the symbol, in bytes. The size is calculated and is actually a best-guess value. In some cases, the value can be zero.

### -param UserContext [in, optional]

The user-defined value specified in 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symenumeratesymbols">SymEnumerateSymbols64</a>, or <b>NULL</b>. Typically, this parameter is used by an application to pass a pointer to a data structure that lets the callback function establish some type of context.

## -returns

If the function returns <b>TRUE</b>, the enumeration will continue.

If the function returns <b>FALSE</b>, the enumeration will stop.

## -remarks

The calling application is called once per symbol until all the symbols are enumerated or until the enumeration callback function returns <b>FALSE</b>.

This callback function supersedes the <i>PSYM_ENUMSYMBOLS_CALLBACK</i> callback function.  <i>PSYM_ENUMSYMBOLS_CALLBACK</i> is defined as follows in Dbghelp.h.


```cpp
#if !defined(_IMAGEHLP_SOURCE_) && defined(_IMAGEHLP64)
#define PSYM_ENUMSYMBOLS_CALLBACK PSYM_ENUMSYMBOLS_CALLBACK64
#define PSYM_ENUMSYMBOLS_CALLBACKW PSYM_ENUMSYMBOLS_CALLBACK64W
#else
typedef BOOL
(CALLBACK *PSYM_ENUMSYMBOLS_CALLBACK)(
    __in PCSTR SymbolName,
    __in ULONG SymbolAddress,
    __in ULONG SymbolSize,
    __in_opt PVOID UserContext
    );

typedef BOOL
(CALLBACK *PSYM_ENUMSYMBOLS_CALLBACKW)(
    __in PCWSTR SymbolName,
    __in ULONG SymbolAddress,
    __in ULONG SymbolSize,
    __in_opt PVOID UserContext
    );
#endif
```

## -see-also

<a href="/windows/desktop/Debug/dbghelp-functions">DbgHelp Functions</a>



<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symenumsymbols">SymEnumSymbols</a>



<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symenumeratesymbols">SymEnumerateSymbols64</a>
