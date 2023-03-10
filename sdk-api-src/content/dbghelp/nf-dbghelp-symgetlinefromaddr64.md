---
UID: NF:dbghelp.SymGetLineFromAddr64
title: SymGetLineFromAddr64 function (dbghelp.h)
description: Locates the source line for the specified address. (SymGetLineFromAddr64)
helpviewer_keywords: ["SymGetLineFromAddr","SymGetLineFromAddr function","SymGetLineFromAddr64","SymGetLineFromAddr64 function","SymGetLineFromAddrW64","_win32_symgetlinefromaddr64","base.symgetlinefromaddr64","dbghelp/SymGetLineFromAddr","dbghelp/SymGetLineFromAddr64","dbghelp/SymGetLineFromAddrW64"]
old-location: base\symgetlinefromaddr64.htm
tech.root: Debug
ms.assetid: a1dad8e0-cd85-41f7-b0e3-e359be94c0ac
ms.date: 12/05/2018
ms.keywords: SymGetLineFromAddr, SymGetLineFromAddr function, SymGetLineFromAddr64, SymGetLineFromAddr64 function, SymGetLineFromAddrW64, _win32_symgetlinefromaddr64, base.symgetlinefromaddr64, dbghelp/SymGetLineFromAddr, dbghelp/SymGetLineFromAddr64, dbghelp/SymGetLineFromAddrW64
req.header: dbghelp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SymGetLineFromAddrW64 (Unicode) and SymGetLineFromAddr64 (ANSI)
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
 - SymGetLineFromAddr64
 - dbghelp/SymGetLineFromAddr64
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
 - SymGetLineFromAddr64
 - SymGetLineFromAddr64
 - SymGetLineFromAddrW64
 - SymGetLineFromAddr
---

## -description

Locates the source line for the specified address.

## -parameters

### -param hProcess [in]

A handle to the process that was originally passed to the 
      <a href="/windows/desktop/api/dbghelp/nf-dbghelp-syminitialize">SymInitialize</a> function.

### -param qwAddr [in]

The address for which a line should be located. It is not necessary for the address to be on a line 
      boundary. If the address appears after the beginning of a line and before the end of the line, the line is 
      found.

### -param pdwDisplacement [out]

The displacement in bytes from the beginning of the line, or zero.

### -param Line64 [out]

A pointer to an <a href="/windows/desktop/api/dbghelp/ns-dbghelp-imagehlp_line">IMAGEHLP_LINE64</a> 
      structure.

## -returns

If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. To retrieve extended error 
       information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The caller must allocate the <i>Line</i> buffer properly and fill in the required members 
    of the <a href="/windows/desktop/api/dbghelp/ns-dbghelp-imagehlp_line">IMAGEHLP_LINE64</a> structure before 
    calling <b>SymGetLineFromAddr64</b>.

This function returns a pointer to a buffer that may be reused by another function. Therefore, be sure to copy 
    the data returned to another buffer immediately.

All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to 
    this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize 
    all concurrent calls from more than one thread to this function.

To call the Unicode version of this function, define <b>DBGHELP_TRANSLATE_TCHAR</b>. 
   <b>SymGetLineFromAddrW64</b> is defined as follows in 
   Dbghelp.h.
   


```cpp
BOOL
IMAGEAPI
SymGetLineFromAddrW64(
    _In_ HANDLE hProcess,
    _In_ DWORD64 dwAddr,
    _Out_ PDWORD pdwDisplacement,
    _Out_ PIMAGEHLP_LINEW64 Line
    );

#ifdef DBGHELP_TRANSLATE_TCHAR
 #define SymGetLineFromAddr64   SymGetLineFromAddrW64
#endif
```


This function supersedes the <b>SymGetLineFromAddr</b> function. For more information, see 
<a href="/windows/desktop/Debug/updated-platform-support">Updated Platform Support</a>. <b>SymGetLineFromAddr</b> is defined as follows in Dbghelp.h. 


```cpp
#if !defined(_IMAGEHLP_SOURCE_) && defined(_IMAGEHLP64)
#define SymGetLineFromAddr SymGetLineFromAddr64
#define SymGetLineFromAddrW SymGetLineFromAddrW64
#else
BOOL
IMAGEAPI
SymGetLineFromAddr(
    _In_ HANDLE hProcess,
    _In_ DWORD dwAddr,
    _Out_ PDWORD pdwDisplacement,
    _Out_ PIMAGEHLP_LINE Line
    );

BOOL
IMAGEAPI
SymGetLineFromAddrW(
    _In_ HANDLE hProcess,
    _In_ DWORD dwAddr,
    _Out_ PDWORD pdwDisplacement,
    _Out_ PIMAGEHLP_LINEW Line
    );
#endif
```



#### Examples

For an example, see 
     <a href="/windows/desktop/Debug/retrieving-symbol-information-by-address">Retrieving Symbol Information by Address</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/Debug/dbghelp-functions">DbgHelp Functions</a>



<a href="/windows/desktop/api/dbghelp/ns-dbghelp-imagehlp_line">IMAGEHLP_LINE64</a>



<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symgetlinefromname">SymGetLineFromName64</a>



<a href="/windows/desktop/api/dbghelp/nf-dbghelp-syminitialize">SymInitialize</a>
