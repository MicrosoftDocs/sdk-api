---
UID: NF:dbghelp.SymGetSymFromName
title: SymGetSymFromName function
author: windows-sdk-content
description: Locates a symbol for the specified name.
old-location: base\symgetsymfromname64.htm
old-project: debug
ms.assetid: 9c9a1a57-06c2-422a-b078-5b7725d54bd4
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: SymGetSymFromName, SymGetSymFromName function, SymGetSymFromName64, SymGetSymFromName64 function, _win32_symgetsymfromname64, base.symgetsymfromname64, dbghelp/SymGetSymFromName, dbghelp/SymGetSymFromName64
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: dbghelp.h
req.include-header: 
req.redist: DbgHelp.dll 5.1 or later
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
 - SymGetSymFromName64
 - SymGetSymFromName
product: Windows
targetos: Windows
req.lib: Dbghelp.lib
req.dll: Dbghelp.dll
req.irql: 
---

# SymGetSymFromName function


## -description


Locates a symbol for the specified name.
<div class="alert"><b>Note</b>  This function is provided only for compatibility. Applications should use 
<a href="https://msdn.microsoft.com/26b9eba7-2038-4640-aeb2-3052889b14ea">SymFromName</a>.</div><div> </div>

## -parameters




### -param hProcess [in]

A handle to the process that was originally passed to the 
<a href="https://msdn.microsoft.com/fb1c98cb-6cd0-4218-aea4-384c24c66395">SymInitialize</a> function.


### -param Name [in]

The symbol name for which a symbol is to be located.


### -param Symbol [in, out]

A pointer to an 
<a href="https://msdn.microsoft.com/7b39281a-c34b-47ae-a3ff-5f0a7a66a588">IMAGEHLP_SYMBOL64</a> structure.


## -returns



If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. To retrieve extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The 
<b>SymGetSymFromName64</b> function is used to locate a symbol for a specified name. The name can contain a module prefix that isolates the symbol search to a single module's symbol table.

The module prefix is in the form of "<i>module</i>!". The "!" character is the delimiter between the module name and the symbol name. If there is no module prefix, then the search is performed on each module's symbol table in a linear manner, beginning with the first module that is loaded.

Using the module prefix is preferable for two reasons. First, the symbol search occurs much faster. Second, when deferred symbol loading is turned on, the search causes symbols to be loaded for each module that is searched. When the symbol is found, the symbol information is copied into the <i>Symbol</i> buffer provided by the caller. The caller must allocate the <i>Symbol</i> buffer properly and fill in the required parameters in the 
<a href="https://msdn.microsoft.com/7b39281a-c34b-47ae-a3ff-5f0a7a66a588">IMAGEHLP_SYMBOL64</a> structure before calling 
<b>SymGetSymFromName64</b>.

All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

This function supersedes the <b>SymGetSymFromName</b> function. For more information, see 
<a href="https://msdn.microsoft.com/34ec8cd3-3260-441d-b55f-4ea21c736eb1">Updated Platform Support</a>. <b>SymGetSymFromName</b> is defined as follows in Dbghelp.h. 

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#if !defined(_IMAGEHLP_SOURCE_) &amp;&amp; defined(_IMAGEHLP64)
#define SymGetSymFromName SymGetSymFromName64
#else
BOOL
IMAGEAPI
SymGetSymFromName(
    __in HANDLE hProcess,
    __in PCSTR Name,
    __inout PIMAGEHLP_SYMBOL Symbol
    );
#endif</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/7b28f70b-2d97-4cc2-8064-dfb806f9cffa">DbgHelp Functions</a>



<a href="https://msdn.microsoft.com/7b39281a-c34b-47ae-a3ff-5f0a7a66a588">IMAGEHLP_SYMBOL64</a>



<a href="https://msdn.microsoft.com/26b9eba7-2038-4640-aeb2-3052889b14ea">SymFromName</a>



<a href="https://msdn.microsoft.com/fb1c98cb-6cd0-4218-aea4-384c24c66395">SymInitialize</a>
 

 

