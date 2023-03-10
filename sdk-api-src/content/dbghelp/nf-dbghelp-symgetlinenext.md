---
UID: NF:dbghelp.SymGetLineNext
title: SymGetLineNext function (dbghelp.h)
description: Retrieves the line information for the next source line. (SymGetLineNext)
helpviewer_keywords: ["SymGetLineNext","SymGetLineNext function","SymGetLineNext64","SymGetLineNext64 function","SymGetLineNextW64","_win32_symgetlinenext64","base.symgetlinenext64","dbghelp/SymGetLineNext","dbghelp/SymGetLineNext64","dbghelp/SymGetLineNextW64"]
old-location: base\symgetlinenext64.htm
tech.root: Debug
ms.assetid: 82adafc3-1080-43bc-b343-eaf59bdef6cb
ms.date: 12/05/2018
ms.keywords: SymGetLineNext, SymGetLineNext function, SymGetLineNext64, SymGetLineNext64 function, SymGetLineNextW64, _win32_symgetlinenext64, base.symgetlinenext64, dbghelp/SymGetLineNext, dbghelp/SymGetLineNext64, dbghelp/SymGetLineNextW64
req.header: dbghelp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SymGetLineNextW64 (Unicode) and SymGetLineNext64 (ANSI)
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
 - SymGetLineNext
 - dbghelp/SymGetLineNext
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
 - SymGetLineNext64
 - SymGetLineNext64
 - SymGetLineNextW64
 - SymGetLineNext
---

# SymGetLineNext function


## -description

Retrieves the line information for the next source line.

## -parameters

### -param hProcess [in]

A handle to the process that was originally passed to the 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-syminitialize">SymInitialize</a> function.

### -param Line [in, out]

A pointer to an 
<a href="/windows/desktop/api/dbghelp/ns-dbghelp-imagehlp_line">IMAGEHLP_LINE64</a> structure that contains the line information.

## -returns

If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. To retrieve extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The 
<b>SymGetLineNext64</b> function requires that the 
<a href="/windows/desktop/api/dbghelp/ns-dbghelp-imagehlp_line">IMAGEHLP_LINE64</a> structure have valid data, presumably obtained from a call to the 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symgetlinefromaddr">SymGetLineFromAddr64</a> or 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symgetlinefromname">SymGetLineFromName64</a> function. This structure receives the line information for the next line in sequence.

This function returns a pointer to a buffer that may be reused by another function. Therefore, be sure to copy the data returned to another buffer immediately.

All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

To call the Unicode version of this function, define DBGHELP_TRANSLATE_TCHAR. <b>SymGetLineNextW64</b> is defined as follows in Dbghelp.h. 


```cpp

BOOL
IMAGEAPI
SymGetLineNextW64(
    __in HANDLE hProcess,
    __inout PIMAGEHLP_LINEW64 Line

#ifdef DBGHELP_TRANSLATE_TCHAR
#define SymGetLineNext64  SymGetLineNextW64
#endif
```


This function supersedes the <b>SymGetLineNext</b> function. For more information, see 
<a href="/windows/desktop/Debug/updated-platform-support">Updated Platform Support</a>. <b>SymGetLineNext</b> is defined as follows in Dbghelp.h. 


```cpp
#if !defined(_IMAGEHLP_SOURCE_) && defined(_IMAGEHLP64)
#define SymGetLineNext SymGetLineNext64
#else
BOOL
IMAGEAPI
SymGetLineNext(
    __in HANDLE hProcess,
    __inout PIMAGEHLP_LINE Line
    );

BOOL
IMAGEAPI
SymGetLineNextW(
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



<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symgetlineprev">SymGetLinePrev64</a>



<a href="/windows/desktop/api/dbghelp/nf-dbghelp-syminitialize">SymInitialize</a>
