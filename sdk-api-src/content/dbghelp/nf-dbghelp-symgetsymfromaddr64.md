---
UID: NF:dbghelp.SymGetSymFromAddr64
title: SymGetSymFromAddr64 function
author: windows-driver-content
description: Locates the symbol for the specified address.
old-location: base\symgetsymfromaddr64.htm
old-project: Debug
ms.assetid: c4882a3b-7773-4ab0-ad83-bdde512b5fb4
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: SymGetSymFromAddr, SymGetSymFromAddr function, SymGetSymFromAddr64, SymGetSymFromAddr64 function, _win32_symgetsymfromaddr64, base.symgetsymfromaddr64, dbghelp/SymGetSymFromAddr, dbghelp/SymGetSymFromAddr64
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
req.unicode-ansi: 
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
-	SymGetSymFromAddr64
-	SymGetSymFromAddr
product: Windows
targetos: Windows
req.lib: Dbghelp.lib
req.dll: Dbghelp.dll
req.irql: 
---

# SymGetSymFromAddr64 function


## -description


Locates the symbol for the specified address.
<div class="alert"><b>Note</b>  This function is provided only for compatibility. Applications should use 
<a href="https://msdn.microsoft.com/20338631-19ab-4ad8-9ba2-56fa4812b33e">SymFromAddr</a>.</div><div> </div>

## -parameters




### -param hProcess [in]

A handle to the process that was originally passed to the 
<a href="https://msdn.microsoft.com/fb1c98cb-6cd0-4218-aea4-384c24c66395">SymInitialize</a> function.


### -param qwAddr

TBD


### -param pdwDisplacement

TBD


### -param Symbol [in, out]

A pointer to an 
<a href="https://msdn.microsoft.com/7b39281a-c34b-47ae-a3ff-5f0a7a66a588">IMAGEHLP_SYMBOL64</a> structure.


#### - Address [in]

The address for which a symbol is to be located. The address does not have to be on a symbol boundary. If the address comes after the beginning of a symbol and before the end of the symbol (the beginning of the symbol plus the symbol size), the symbol is found.


#### - Displacement [out, optional]

The displacement from the beginning of the symbol, or zero.


## -returns



If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. To retrieve extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The 
<b>SymGetSymFromAddr64</b> function locates the symbol for a specified address. The modules are searched for the one the address belongs to. When the module is found, its symbol table is searched for a match. When the symbol is found, the symbol information is copied into the <i>Symbol</i> buffer provided by the caller. The caller must allocate the <i>Symbol</i> buffer properly and fill in the required parameters in the 
<a href="https://msdn.microsoft.com/7b39281a-c34b-47ae-a3ff-5f0a7a66a588">IMAGEHLP_SYMBOL64</a> structure before calling 
<b>SymGetSymFromAddr64</b>.

All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

This function supersedes the <b>SymGetSymFromAddr</b> function. For more information, see 
<a href="https://msdn.microsoft.com/34ec8cd3-3260-441d-b55f-4ea21c736eb1">Updated Platform Support</a>. <b>SymGetSymFromAddr</b> is defined as follows in Dbghelp.h. 

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#if !defined(_IMAGEHLP_SOURCE_) &amp;&amp; defined(_IMAGEHLP64)
#define SymGetSymFromAddr SymGetSymFromAddr64
#else
BOOL
IMAGEAPI
SymGetSymFromAddr(
    __in HANDLE hProcess,
    __in DWORD dwAddr,
    __out_opt PDWORD pdwDisplacement,
    __inout PIMAGEHLP_SYMBOL Symbol
    );
#endif</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/7b28f70b-2d97-4cc2-8064-dfb806f9cffa">DbgHelp Functions</a>



<a href="https://msdn.microsoft.com/7b39281a-c34b-47ae-a3ff-5f0a7a66a588">IMAGEHLP_SYMBOL64</a>



<a href="https://msdn.microsoft.com/20338631-19ab-4ad8-9ba2-56fa4812b33e">SymFromAddr</a>



<a href="https://msdn.microsoft.com/fb1c98cb-6cd0-4218-aea4-384c24c66395">SymInitialize</a>
 

 

