---
UID: NF:dbghelp.SymGetLinePrev
title: SymGetLinePrev function (dbghelp.h)
description: Retrieves the line information for the previous source line. (SymGetLinePrev)
helpviewer_keywords: ["SymGetLinePrev","SymGetLinePrev function","SymGetLinePrev64","SymGetLinePrev64 function","SymGetLinePrevW64","_win32_symgetlineprev64","base.symgetlineprev64","dbghelp/SymGetLinePrev","dbghelp/SymGetLinePrev64","dbghelp/SymGetLinePrevW64"]
old-location: base\symgetlineprev64.htm
tech.root: Debug
ms.assetid: 7f6d0f20-5dfa-4d6c-8551-1dbc3cc54176
ms.date: 12/05/2018
ms.keywords: SymGetLinePrev, SymGetLinePrev function, SymGetLinePrev64, SymGetLinePrev64 function, SymGetLinePrevW64, _win32_symgetlineprev64, base.symgetlineprev64, dbghelp/SymGetLinePrev, dbghelp/SymGetLinePrev64, dbghelp/SymGetLinePrevW64
req.header: dbghelp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SymGetLinePrevW64 (Unicode) and SymGetLinePrev64 (ANSI)
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
 - SymGetLinePrev
 - dbghelp/SymGetLinePrev
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
 - SymGetLinePrev64
 - SymGetLinePrev64
 - SymGetLinePrevW64
 - SymGetLinePrev
---

# SymGetLinePrev function


## -description

Retrieves the line information for the previous source line.

## -parameters

### -param hProcess [in]

A handle to the process that was originally passed to the 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-syminitialize">SymInitialize</a> function.

### -param Line [in, out]

A pointer to an 
<a href="/windows/desktop/api/dbghelp/ns-dbghelp-imagehlp_line">IMAGEHLP_LINE64</a> structure.

## -returns

If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. To retrieve extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The 
<b>SymGetLinePrev64</b> function requires that the 
<a href="/windows/desktop/api/dbghelp/ns-dbghelp-imagehlp_line">IMAGEHLP_LINE64</a> structure have valid data, presumably obtained from a call to the 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symgetlinefromaddr">SymGetLineFromAddr64</a> or 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symgetlinefromname">SymGetLineFromName64</a> function. This structure is filled with the line information for the previous line in sequence.

This function returns a pointer to a buffer that may be reused by another function. Therefore, be sure to copy the data returned to another buffer immediately.

All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

To call the Unicode version of this function, define DBGHELP_TRANSLATE_TCHAR. <b>SymGetLinePrevW64</b> is defined as follows in DbgHelp.h. 


```cpp
BOOL
IMAGEAPI
SymGetLinePrevW64(
    __in HANDLE hProcess,
    __inout PIMAGEHLP_LINEW64 Line
    );

#ifdef DBGHELP_TRANSLATE_TCHAR
#define SymGetLinePrev64    SymGetLinePrevW64
#endif
```


This function supersedes the <b>SymGetLinePrev</b> function. For more information, see 
<a href="/windows/desktop/Debug/updated-platform-support">Updated Platform Support</a>. <b>SymGetLinePrev</b> is defined as follows in DbgHelp.h. 


```cpp
#if !defined(_IMAGEHLP_SOURCE_) && defined(_IMAGEHLP64)
#define SymGetLinePrev SymGetLinePrev64
#else
BOOL
IMAGEAPI
SymGetLinePrev(
    __in HANDLE hProcess,
    __inout PIMAGEHLP_LINE Line
    );

BOOL
IMAGEAPI
SymGetLinePrevW(
    __in HANDLE hProcess,
    __inout PIMAGEHLP_LINEW Line
    );
#endif
```

## -see-also

<a href="/windows/desktop/Debug/dbghelp-functions">DbgHelp Functions</a>



<a href="/windows/desktop/api/dbghelp/ns-dbghelp-imagehlp_line">IMAGEHLP_LINE64</a>



<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symgetlinefromaddr">SymGetLineFromAddr64</a>



<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symgetlinefromname">SymGetLineFromName64</a>



<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symgetlinenext">SymGetLineNext64</a>



<a href="/windows/desktop/api/dbghelp/nf-dbghelp-syminitialize">SymInitialize</a>
