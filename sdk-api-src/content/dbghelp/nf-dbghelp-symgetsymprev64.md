---
UID: NF:dbghelp.SymGetSymPrev64
title: SymGetSymPrev64 function
author: windows-sdk-content
description: Retrieves the symbol information for the previous symbol.
old-location: base\symgetsymprev64.htm
tech.root: debug
ms.assetid: dbb1353b-5cc1-4986-a2b5-f67be7189ea8
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: SymGetSymPrev, SymGetSymPrev function, SymGetSymPrev64, SymGetSymPrev64 function, _win32_symgetsymprev64, base.symgetsymprev64, dbghelp/SymGetSymPrev, dbghelp/SymGetSymPrev64
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: DbgHelp.dll 5.1 or later
---

# SymGetSymPrev64 function


## -description


Retrieves the symbol information for the previous symbol.
<div class="alert"><b>Note</b>  This function is provided only for compatibility. Applications should use 
<a href="https://msdn.microsoft.com/45503f0c-cb66-4ddf-986d-02de7fc480f2">SymPrev</a>.</div><div> </div>

## -parameters




### -param hProcess [in]

A handle to the process that was originally passed to the 
<a href="https://msdn.microsoft.com/fb1c98cb-6cd0-4218-aea4-384c24c66395">SymInitialize</a> function.


### -param Symbol [in, out]

A pointer to an 
<a href="https://msdn.microsoft.com/7b39281a-c34b-47ae-a3ff-5f0a7a66a588">IMAGEHLP_SYMBOL64</a> structure.


## -returns



If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. To retrieve extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The 
<b>SymGetSymPrev64</b> function requires the <a href="https://msdn.microsoft.com/7b39281a-c34b-47ae-a3ff-5f0a7a66a588">IMAGEHLP_SYMBOL64</a> structure to have valid data, presumably obtained from a call to the 
<a href="https://msdn.microsoft.com/c4882a3b-7773-4ab0-ad83-bdde512b5fb4">SymGetSymFromAddr64</a> or 
<a href="https://msdn.microsoft.com/9c9a1a57-06c2-422a-b078-5b7725d54bd4">SymGetSymFromName64</a> function. This structure is filled in with the symbol information for the previous symbol in sequence by virtual address.

All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

To call the Unicode version of this function, define DBGHELP_TRANSLATE_TCHAR. <b>SymGetSymPrevW64</b> is defined as follows in DbgHelp.h. 

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>BOOL
IMAGEAPI
SymGetSymPrevW64(
    __in HANDLE hProcess,
    __inout PIMAGEHLP_SYMBOLW64 Symbol
    );</pre>
</td>
</tr>
</table></span></div>
This function supersedes the <b>SymGetSymPrev</b> function. For more information, see 
<a href="https://msdn.microsoft.com/34ec8cd3-3260-441d-b55f-4ea21c736eb1">Updated Platform Support</a>. <b>SymGetSymPrev</b> is defined as follows in Dbghelp.h. 

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#if !defined(_IMAGEHLP_SOURCE_) &amp;&amp; defined(_IMAGEHLP64)
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
#endif</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/7b28f70b-2d97-4cc2-8064-dfb806f9cffa">DbgHelp Functions</a>



<a href="https://msdn.microsoft.com/7b39281a-c34b-47ae-a3ff-5f0a7a66a588">IMAGEHLP_SYMBOL64</a>



<a href="https://msdn.microsoft.com/c4882a3b-7773-4ab0-ad83-bdde512b5fb4">SymGetSymFromAddr64</a>



<a href="https://msdn.microsoft.com/9c9a1a57-06c2-422a-b078-5b7725d54bd4">SymGetSymFromName64</a>



<a href="https://msdn.microsoft.com/e58f21b9-c2fc-48f6-af45-3c9ec42809c1">SymGetSymNext64</a>



<a href="https://msdn.microsoft.com/fb1c98cb-6cd0-4218-aea4-384c24c66395">SymInitialize</a>
 

 

