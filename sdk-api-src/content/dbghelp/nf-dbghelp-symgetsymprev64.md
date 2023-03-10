---
UID: NF:dbghelp.SymGetSymPrev64
title: SymGetSymPrev64 function (dbghelp.h)
description: Retrieves the symbol information for the previous symbol. (SymGetSymPrev64)
helpviewer_keywords: ["SymGetSymPrev","SymGetSymPrev function","SymGetSymPrev64","SymGetSymPrev64 function","_win32_symgetsymprev64","base.symgetsymprev64","dbghelp/SymGetSymPrev","dbghelp/SymGetSymPrev64"]
old-location: base\symgetsymprev64.htm
tech.root: Debug
ms.assetid: dbb1353b-5cc1-4986-a2b5-f67be7189ea8
ms.date: 12/05/2018
ms.keywords: SymGetSymPrev, SymGetSymPrev function, SymGetSymPrev64, SymGetSymPrev64 function, _win32_symgetsymprev64, base.symgetsymprev64, dbghelp/SymGetSymPrev, dbghelp/SymGetSymPrev64
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
 - SymGetSymPrev64
 - dbghelp/SymGetSymPrev64
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
 - SymGetSymPrev64
 - SymGetSymPrev
---

# SymGetSymPrev64 function


## -description

Retrieves the symbol information for the previous symbol.
<div class="alert"><b>Note</b>  This function is provided only for compatibility. Applications should use 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symprev">SymPrev</a>.</div><div> </div>

## -parameters

### -param hProcess [in]

A handle to the process that was originally passed to the 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-syminitialize">SymInitialize</a> function.

### -param Symbol [in, out]

A pointer to an 
<a href="/windows/desktop/api/dbghelp/ns-dbghelp-imagehlp_symbol">IMAGEHLP_SYMBOL64</a> structure.

## -returns

If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. To retrieve extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The 
<b>SymGetSymPrev64</b> function requires the <a href="/windows/desktop/api/dbghelp/ns-dbghelp-imagehlp_symbol">IMAGEHLP_SYMBOL64</a> structure to have valid data, presumably obtained from a call to the 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symgetsymfromaddr">SymGetSymFromAddr64</a> or 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symgetsymfromname">SymGetSymFromName64</a> function. This structure is filled in with the symbol information for the previous symbol in sequence by virtual address.

All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

To call the Unicode version of this function, define DBGHELP_TRANSLATE_TCHAR. <b>SymGetSymPrevW64</b> is defined as follows in DbgHelp.h. 


```cpp
BOOL
IMAGEAPI
SymGetSymPrevW64(
    __in HANDLE hProcess,
    __inout PIMAGEHLP_SYMBOLW64 Symbol
    );
```


This function supersedes the <b>SymGetSymPrev</b> function. For more information, see 
<a href="/windows/desktop/Debug/updated-platform-support">Updated Platform Support</a>. <b>SymGetSymPrev</b> is defined as follows in Dbghelp.h. 


```cpp
#if !defined(_IMAGEHLP_SOURCE_) && defined(_IMAGEHLP64)
#define SymGetSymPrev SymGetSymPrev64
#define SymGetSymPrevW SymGetSymPrevW64
#else
BOOL
IMAGEAPI
SymGetSymPrev(
    __in HANDLE hProcess,
    __inout PIMAGEHLP_SYMBOL Symbol
    );

BOOL
IMAGEAPI
SymGetSymPrevW(
    __in HANDLE hProcess,
    __inout PIMAGEHLP_SYMBOLW Symbol
    );
#endif
```

## -see-also

<a href="/windows/desktop/Debug/dbghelp-functions">DbgHelp Functions</a>



<a href="/windows/desktop/api/dbghelp/ns-dbghelp-imagehlp_symbol">IMAGEHLP_SYMBOL64</a>



<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symgetsymfromaddr">SymGetSymFromAddr64</a>



<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symgetsymfromname">SymGetSymFromName64</a>



<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symgetsymnext">SymGetSymNext64</a>



<a href="/windows/desktop/api/dbghelp/nf-dbghelp-syminitialize">SymInitialize</a>
