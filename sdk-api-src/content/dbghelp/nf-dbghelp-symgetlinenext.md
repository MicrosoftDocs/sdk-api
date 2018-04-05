---
UID: NF:dbghelp.SymGetLineNext
title: SymGetLineNext function
author: windows-driver-content
description: Retrieves the line information for the next source line.
old-location: base\symgetlinenext64.htm
old-project: Debug
ms.assetid: 82adafc3-1080-43bc-b343-eaf59bdef6cb
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: SymGetLineNext, SymGetLineNext function, SymGetLineNext64, SymGetLineNext64 function, SymGetLineNextW64, _win32_symgetlinenext64, base.symgetlinenext64, dbghelp/SymGetLineNext, dbghelp/SymGetLineNext64, dbghelp/SymGetLineNextW64
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
req.unicode-ansi: SymGetLineNextW64 (Unicode) and SymGetLineNext64 (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: IMAGEHLP_SYMBOL_TYPE_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Dbghelp.dll
api_name:
-	SymGetLineNext64
-	SymGetLineNext64
-	SymGetLineNextW64
-	SymGetLineNext
product: Windows
targetos: Windows
req.lib: Dbghelp.lib
req.dll: Dbghelp.dll
req.irql: 
---

# SymGetLineNext function


## -description


Retrieves the line information for the next source line.


## -parameters




### -param hProcess [in]

A handle to the process that was originally passed to the 
<a href="https://msdn.microsoft.com/fb1c98cb-6cd0-4218-aea4-384c24c66395">SymInitialize</a> function.


### -param Line [in, out]

A pointer to an 
<a href="https://msdn.microsoft.com/62124983-8381-4eb4-94f6-220b844aca45">IMAGEHLP_LINE64</a> structure that contains the line information.


## -returns



If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. To retrieve extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The 
<b>SymGetLineNext64</b> function requires that the 
<a href="https://msdn.microsoft.com/62124983-8381-4eb4-94f6-220b844aca45">IMAGEHLP_LINE64</a> structure have valid data, presumably obtained from a call to the 
<a href="https://msdn.microsoft.com/a1dad8e0-cd85-41f7-b0e3-e359be94c0ac">SymGetLineFromAddr64</a> or 
<a href="https://msdn.microsoft.com/cb8870f6-1bae-40df-842e-ec3ca0167691">SymGetLineFromName64</a> function. This structure receives the line information for the next line in sequence.

This function returns a pointer to a buffer that may be reused by another function. Therefore, be sure to copy the data returned to another buffer immediately.

All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

To call the Unicode version of this function, define DBGHELP_TRANSLATE_TCHAR. <b>SymGetLineNextW64</b> is defined as follows in Dbghelp.h. 

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
BOOL
IMAGEAPI
SymGetLineNextW64(
    __in HANDLE hProcess,
    __inout PIMAGEHLP_LINEW64 Line

#ifdef DBGHELP_TRANSLATE_TCHAR
#define SymGetLineNext64  SymGetLineNextW64
#endif</pre>
</td>
</tr>
</table></span></div>
This function supersedes the <b>SymGetLineNext</b> function. For more information, see 
<a href="https://msdn.microsoft.com/34ec8cd3-3260-441d-b55f-4ea21c736eb1">Updated Platform Support</a>. <b>SymGetLineNext</b> is defined as follows in Dbghelp.h. 

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#if !defined(_IMAGEHLP_SOURCE_) &amp;&amp; defined(_IMAGEHLP64)
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
#endif</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/7b28f70b-2d97-4cc2-8064-dfb806f9cffa">DbgHelp Functions</a>



<a href="https://msdn.microsoft.com/62124983-8381-4eb4-94f6-220b844aca45">IMAGEHLP_LINE64</a>



<a href="https://msdn.microsoft.com/a1dad8e0-cd85-41f7-b0e3-e359be94c0ac">SymGetLineFromAddr64</a>



<a href="https://msdn.microsoft.com/cb8870f6-1bae-40df-842e-ec3ca0167691">SymGetLineFromName64</a>



<a href="https://msdn.microsoft.com/7f6d0f20-5dfa-4d6c-8551-1dbc3cc54176">SymGetLinePrev64</a>



<a href="https://msdn.microsoft.com/fb1c98cb-6cd0-4218-aea4-384c24c66395">SymInitialize</a>
 

 

