---
UID: NF:dbghelp.SymGetLineFromName
title: SymGetLineFromName function (dbghelp.h)
description: Locates a source line for the specified module, file name, and line number. (SymGetLineFromName)
helpviewer_keywords: ["SymGetLineFromName","SymGetLineFromName function","SymGetLineFromName64","SymGetLineFromName64 function","SymGetLineFromNameW64","_win32_symgetlinefromname64","base.symgetlinefromname64","dbghelp/SymGetLineFromName","dbghelp/SymGetLineFromName64","dbghelp/SymGetLineFromNameW64"]
old-location: base\symgetlinefromname64.htm
tech.root: Debug
ms.assetid: cb8870f6-1bae-40df-842e-ec3ca0167691
ms.date: 12/05/2018
ms.keywords: SymGetLineFromName, SymGetLineFromName function, SymGetLineFromName64, SymGetLineFromName64 function, SymGetLineFromNameW64, _win32_symgetlinefromname64, base.symgetlinefromname64, dbghelp/SymGetLineFromName, dbghelp/SymGetLineFromName64, dbghelp/SymGetLineFromNameW64
req.header: dbghelp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SymGetLineFromNameW64 (Unicode) and SymGetLineFromName64 (ANSI)
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
 - SymGetLineFromName
 - dbghelp/SymGetLineFromName
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
 - SymGetLineFromName64
 - SymGetLineFromName64
 - SymGetLineFromNameW64
 - SymGetLineFromName
---

# SymGetLineFromName function


## -description

Locates a source line for the specified module, file name, and line number.

## -parameters

### -param hProcess [in]

A handle to the process that was originally passed to the 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-syminitialize">SymInitialize</a> function.

### -param ModuleName [in, optional]

The name of the module in which a line is to be located.

### -param FileName [in, optional]

The name of the file in which a line is to be located. If the application has more than one source file with this name, be sure to specify a full path.

### -param dwLineNumber [in]

The line number to be located.

### -param plDisplacement [out]

The displacement in bytes from the beginning of the line, or zero.

### -param Line [in, out]

A pointer to an 
<a href="/windows/desktop/api/dbghelp/ns-dbghelp-imagehlp_line">IMAGEHLP_LINE64</a> structure.

## -returns

If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. To retrieve extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The caller must allocate the <i>Line</i> buffer properly and fill in the required members of the 
<a href="/windows/desktop/api/dbghelp/ns-dbghelp-imagehlp_line">IMAGEHLP_LINE64</a> structure before calling 
<b>SymGetLineFromName64</b>.

Before calling this function, ensure that the symbols are initialized correctly by first calling 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-syminitialize">SymInitialize</a>, 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symsetoptions">SymSetOptions</a>, and 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symloadmodule">SymLoadModule64</a>.

This function returns a pointer to a buffer that may be reused by another function. Therefore, be sure to copy the data returned to another buffer immediately.

All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

To call the Unicode version of this function, define DBGHELP_TRANSLATE_TCHAR. <b>SymGetLineFromNameW64</b> is defined as follows in Dbghelp.h. 


```cpp

BOOL
IMAGEAPI
SymGetLineFromNameW64(
    __in HANDLE hProcess,
    __in_opt PCWSTR ModuleName,
    __in_opt PCWSTR FileName,
    __in DWORD dwLineNumber,
    __out PLONG plDisplacement,
    __inout PIMAGEHLP_LINEW64 Line
    );

#ifdef DBGHELP_TRANSLATE_TCHAR
#define SymGetLineFromName64   SymGetLineFromNameW64
#endif
```


This function supersedes the <b>SymGetLineFromName</b> function. For more information, see 
<a href="/windows/desktop/Debug/updated-platform-support">Updated Platform Support</a>. <b>SymGetLineFromName</b> is defined as follows in Dbghelp.h. 


```cpp
#if !defined(_IMAGEHLP_SOURCE_) && defined(_IMAGEHLP64)
#define SymGetLineFromName SymGetLineFromName64
#else
BOOL
IMAGEAPI
SymGetLineFromName(
    __in HANDLE hProcess,
    __in_opt PCSTR ModuleName,
    __in_opt PCSTR FileName,
    __in DWORD dwLineNumber,
    __out PLONG plDisplacement,
    __inout PIMAGEHLP_LINE Line
    );
#endif
```



#### Examples

For an example, see 
<a href="/windows/desktop/Debug/retrieving-symbol-information-by-name">Retrieving Symbol Information by Name</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/Debug/dbghelp-functions">DbgHelp Functions</a>



<a href="/windows/desktop/api/dbghelp/ns-dbghelp-imagehlp_line">IMAGEHLP_LINE64</a>



<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symgetlinefromaddr">SymGetLineFromAddr64</a>



<a href="/windows/desktop/api/dbghelp/nf-dbghelp-syminitialize">SymInitialize</a>
