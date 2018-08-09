---
UID: NF:dbghelp.SymGetLinePrev64
title: SymGetLinePrev64 function
author: windows-sdk-content
description: Retrieves the line information for the previous source line.
old-location: base\symgetlineprev64.htm
old-project: debug
ms.assetid: 7f6d0f20-5dfa-4d6c-8551-1dbc3cc54176
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: SymGetLinePrev, SymGetLinePrev function, SymGetLinePrev64, SymGetLinePrev64 function, SymGetLinePrevW64, _win32_symgetlineprev64, base.symgetlineprev64, dbghelp/SymGetLinePrev, dbghelp/SymGetLinePrev64, dbghelp/SymGetLinePrevW64
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: IMAGEHLP_SYMBOL_TYPE_INFO
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
product: Windows
targetos: Windows
req.lib: Dbghelp.lib
req.dll: Dbghelp.dll
req.irql: 
---

# SymGetLinePrev64 function


## -description


Retrieves the line information for the previous source line.


## -parameters




### -param hProcess [in]

A handle to the process that was originally passed to the 
<a href="https://msdn.microsoft.com/fb1c98cb-6cd0-4218-aea4-384c24c66395">SymInitialize</a> function.


### -param Line [in, out]

A pointer to an 
<a href="https://msdn.microsoft.com/62124983-8381-4eb4-94f6-220b844aca45">IMAGEHLP_LINE64</a> structure.


## -returns



If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. To retrieve extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The 
<b>SymGetLinePrev64</b> function requires that the 
<a href="https://msdn.microsoft.com/62124983-8381-4eb4-94f6-220b844aca45">IMAGEHLP_LINE64</a> structure have valid data, presumably obtained from a call to the 
<a href="https://msdn.microsoft.com/a1dad8e0-cd85-41f7-b0e3-e359be94c0ac">SymGetLineFromAddr64</a> or 
<a href="https://msdn.microsoft.com/cb8870f6-1bae-40df-842e-ec3ca0167691">SymGetLineFromName64</a> function. This structure is filled with the line information for the previous line in sequence.

This function returns a pointer to a buffer that may be reused by another function. Therefore, be sure to copy the data returned to another buffer immediately.

All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

To call the Unicode version of this function, define DBGHELP_TRANSLATE_TCHAR. <b>SymGetLinePrevW64</b> is defined as follows in DbgHelp.h. 

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>BOOL
IMAGEAPI
SymGetLinePrevW64(
    __in HANDLE hProcess,
    __inout PIMAGEHLP_LINEW64 Line
    );

#ifdef DBGHELP_TRANSLATE_TCHAR
#define SymGetLinePrev64    SymGetLinePrevW64
#endif</pre>
</td>
</tr>
</table></span></div>
This function supersedes the <b>SymGetLinePrev</b> function. For more information, see 
<a href="https://msdn.microsoft.com/34ec8cd3-3260-441d-b55f-4ea21c736eb1">Updated Platform Support</a>. <b>SymGetLinePrev</b> is defined as follows in DbgHelp.h. 

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#if !defined(_IMAGEHLP_SOURCE_) &amp;&amp; defined(_IMAGEHLP64)
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
#endif</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/7b28f70b-2d97-4cc2-8064-dfb806f9cffa">DbgHelp Functions</a>



<a href="https://msdn.microsoft.com/62124983-8381-4eb4-94f6-220b844aca45">IMAGEHLP_LINE64</a>



<a href="https://msdn.microsoft.com/a1dad8e0-cd85-41f7-b0e3-e359be94c0ac">SymGetLineFromAddr64</a>



<a href="https://msdn.microsoft.com/cb8870f6-1bae-40df-842e-ec3ca0167691">SymGetLineFromName64</a>



<a href="https://msdn.microsoft.com/82adafc3-1080-43bc-b343-eaf59bdef6cb">SymGetLineNext64</a>



<a href="https://msdn.microsoft.com/fb1c98cb-6cd0-4218-aea4-384c24c66395">SymInitialize</a>
 

 

