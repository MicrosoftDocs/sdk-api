---
UID: NF:dbghelp.SymGetSymFromName
title: SymGetSymFromName function (dbghelp.h)
description: Locates a symbol for the specified name. (SymGetSymFromName)
helpviewer_keywords: ["SymGetSymFromName","SymGetSymFromName function","SymGetSymFromName64","SymGetSymFromName64 function","_win32_symgetsymfromname64","base.symgetsymfromname64","dbghelp/SymGetSymFromName","dbghelp/SymGetSymFromName64"]
old-location: base\symgetsymfromname64.htm
tech.root: Debug
ms.assetid: 9c9a1a57-06c2-422a-b078-5b7725d54bd4
ms.date: 12/05/2018
ms.keywords: SymGetSymFromName, SymGetSymFromName function, SymGetSymFromName64, SymGetSymFromName64 function, _win32_symgetsymfromname64, base.symgetsymfromname64, dbghelp/SymGetSymFromName, dbghelp/SymGetSymFromName64
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
 - SymGetSymFromName
 - dbghelp/SymGetSymFromName
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
 - SymGetSymFromName64
 - SymGetSymFromName
---

# SymGetSymFromName function


## -description

Locates a symbol for the specified name.
<div class="alert"><b>Note</b>  This function is provided only for compatibility. Applications should use 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symfromname">SymFromName</a>.</div><div> </div>

## -parameters

### -param hProcess [in]

A handle to the process that was originally passed to the 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-syminitialize">SymInitialize</a> function.

### -param Name [in]

The symbol name for which a symbol is to be located.

### -param Symbol [in, out]

A pointer to an 
<a href="/windows/desktop/api/dbghelp/ns-dbghelp-imagehlp_symbol">IMAGEHLP_SYMBOL64</a> structure.

## -returns

If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. To retrieve extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The 
<b>SymGetSymFromName64</b> function is used to locate a symbol for a specified name. The name can contain a module prefix that isolates the symbol search to a single module's symbol table.

The module prefix is in the form of "<i>module</i>!". The "!" character is the delimiter between the module name and the symbol name. If there is no module prefix, then the search is performed on each module's symbol table in a linear manner, beginning with the first module that is loaded.

Using the module prefix is preferable for two reasons. First, the symbol search occurs much faster. Second, when deferred symbol loading is turned on, the search causes symbols to be loaded for each module that is searched. When the symbol is found, the symbol information is copied into the <i>Symbol</i> buffer provided by the caller. The caller must allocate the <i>Symbol</i> buffer properly and fill in the required parameters in the 
<a href="/windows/desktop/api/dbghelp/ns-dbghelp-imagehlp_symbol">IMAGEHLP_SYMBOL64</a> structure before calling 
<b>SymGetSymFromName64</b>.

All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

This function supersedes the <b>SymGetSymFromName</b> function. For more information, see 
<a href="/windows/desktop/Debug/updated-platform-support">Updated Platform Support</a>. <b>SymGetSymFromName</b> is defined as follows in Dbghelp.h. 


```cpp
#if !defined(_IMAGEHLP_SOURCE_) && defined(_IMAGEHLP64)
#define SymGetSymFromName SymGetSymFromName64
#else
BOOL
IMAGEAPI
SymGetSymFromName(
    __in HANDLE hProcess,
    __in PCSTR Name,
    __inout PIMAGEHLP_SYMBOL Symbol
    );
#endif
```

## -see-also

<a href="/windows/desktop/Debug/dbghelp-functions">DbgHelp Functions</a>



<a href="/windows/desktop/api/dbghelp/ns-dbghelp-imagehlp_symbol">IMAGEHLP_SYMBOL64</a>



<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symfromname">SymFromName</a>



<a href="/windows/desktop/api/dbghelp/nf-dbghelp-syminitialize">SymInitialize</a>
