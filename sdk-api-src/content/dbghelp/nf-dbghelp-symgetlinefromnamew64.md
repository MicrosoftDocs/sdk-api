---
UID: NF:dbghelp.SymGetLineFromNameW64
title: SymGetLineFromNameW64 function
author: windows-sdk-content
description: Locates a source line for the specified module, file name, and line number.
old-location: base\symgetlinefromname64.htm
tech.root: debug
ms.assetid: cb8870f6-1bae-40df-842e-ec3ca0167691
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: SymGetLineFromName, SymGetLineFromName function, SymGetLineFromName64, SymGetLineFromName64 function, SymGetLineFromNameW64, _win32_symgetlinefromname64, base.symgetlinefromname64, dbghelp/SymGetLineFromName, dbghelp/SymGetLineFromName64, dbghelp/SymGetLineFromNameW64
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: DbgHelp.dll 5.1 or later
---

# SymGetLineFromNameW64 function


## -description


Locates a source line for the specified module, file name, and line number.


## -parameters




### -param hProcess [in]

A handle to the process that was originally passed to the 
<a href="https://msdn.microsoft.com/fb1c98cb-6cd0-4218-aea4-384c24c66395">SymInitialize</a> function.


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
<a href="https://msdn.microsoft.com/62124983-8381-4eb4-94f6-220b844aca45">IMAGEHLP_LINE64</a> structure.


## -returns



If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. To retrieve extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The caller must allocate the <i>Line</i> buffer properly and fill in the required members of the 
<a href="https://msdn.microsoft.com/62124983-8381-4eb4-94f6-220b844aca45">IMAGEHLP_LINE64</a> structure before calling 
<b>SymGetLineFromName64</b>.

Before calling this function, ensure that the symbols are initialized correctly by first calling 
<a href="https://msdn.microsoft.com/fb1c98cb-6cd0-4218-aea4-384c24c66395">SymInitialize</a>, 
<a href="https://msdn.microsoft.com/15d72415-829f-4ba3-af80-1f3762cbebda">SymSetOptions</a>, and 
<a href="https://msdn.microsoft.com/be50588b-066b-42ab-ba81-7537c811676f">SymLoadModule64</a>.

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
<a href="https://msdn.microsoft.com/34ec8cd3-3260-441d-b55f-4ea21c736eb1">Updated Platform Support</a>. <b>SymGetLineFromName</b> is defined as follows in Dbghelp.h. 


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
<a href="https://msdn.microsoft.com/d3a9d73e-fb77-4be3-a881-c258bcc587fe">Retrieving Symbol Information by Name</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/7b28f70b-2d97-4cc2-8064-dfb806f9cffa">DbgHelp Functions</a>



<a href="https://msdn.microsoft.com/62124983-8381-4eb4-94f6-220b844aca45">IMAGEHLP_LINE64</a>



<a href="https://msdn.microsoft.com/a1dad8e0-cd85-41f7-b0e3-e359be94c0ac">SymGetLineFromAddr64</a>



<a href="https://msdn.microsoft.com/fb1c98cb-6cd0-4218-aea4-384c24c66395">SymInitialize</a>
 

 

