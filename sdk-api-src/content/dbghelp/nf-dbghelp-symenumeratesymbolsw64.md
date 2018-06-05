---
UID: NF:dbghelp.SymEnumerateSymbolsW64
title: SymEnumerateSymbolsW64 function
author: windows-sdk-content
description: Enumerates all the symbols for a specified module.
old-location: base\symenumeratesymbols64.htm
old-project: Debug
ms.assetid: f1aa710c-fbe5-4c9a-9956-5bd872b4b5be
ms.author: windowssdkdev
ms.date: 05/17/2018
ms.keywords: SymEnumerateSymbols, SymEnumerateSymbols function, SymEnumerateSymbols64, SymEnumerateSymbols64 function, SymEnumerateSymbolsW, SymEnumerateSymbolsW64, _win32_symenumeratesymbols64, base.symenumeratesymbols64, dbghelp/SymEnumerateSymbols, dbghelp/SymEnumerateSymbols64, dbghelp/SymEnumerateSymbolsW, dbghelp/SymEnumerateSymbolsW64
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
req.unicode-ansi: SymEnumerateSymbolsW64 (Unicode) and SymEnumerateSymbols64 (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: IMAGEHLP_SYMBOL_TYPE_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Dbghelp.dll
api_name:
-	SymEnumerateSymbols64
-	SymEnumerateSymbols64
-	SymEnumerateSymbolsW64
-	SymEnumerateSymbols
-	SymEnumerateSymbolsW
product: Windows
targetos: Windows
req.lib: Dbghelp.lib
req.dll: Dbghelp.dll
req.irql: 
---

# SymEnumerateSymbolsW64 function


## -description


Enumerates all the symbols for a specified module.
<div class="alert"><b>Note</b>  This function is provided only for compatibility. Applications should use 
<a href="https://msdn.microsoft.com/e1232657-baf6-4e5b-9995-a382aa1391c2">SymEnumSymbols</a>, which is faster and more powerful.</div><div> </div>

## -parameters




### -param hProcess [in]

A handle to the process. This handle must have been previously passed to the 
<a href="https://msdn.microsoft.com/fb1c98cb-6cd0-4218-aea4-384c24c66395">SymInitialize</a> function.


### -param BaseOfDll [in]

The base address of the module for which symbols are to be enumerated.


### -param EnumSymbolsCallback [in]

The callback function that receives the symbol information. For more information, see 
<a href="https://msdn.microsoft.com/e1430398-041f-4edd-b7b0-de3a60a42b37">SymEnumerateSymbolsProc64</a>.


### -param UserContext [in, optional]

A user-defined value or <b>NULL</b>. This value is passed to the callback function. Typically, this parameter is used by an application to pass a pointer to a data structure that enables the callback function establish some type of context.


## -returns



If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. To retrieve extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The 
<b>SymEnumerateSymbols64</b> function enumerates all the symbols for the specified module. The module information is located by the <i>BaseOfDll</i> parameter. The callback function is called once per symbol and is passed the information for each symbol.

All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

The Unicode version of this function, <b>SymEnumerateSymbolsW64</b> is defined as follows in Dbghelp.h. 

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
BOOL
IMAGEAPI
SymEnumerateSymbolsW64(
    __in HANDLE hProcess,
    __in ULONG64 BaseOfDll,
    __in PSYM_ENUMSYMBOLS_CALLBACK64W EnumSymbolsCallback,
    __in_opt PVOID UserContext
    );</pre>
</td>
</tr>
</table></span></div>
This function supersedes the <b>SymEnumerateSymbols</b> function. For more information, see 
<a href="https://msdn.microsoft.com/34ec8cd3-3260-441d-b55f-4ea21c736eb1">Updated Platform Support</a>. <b>SymEnumerateSymbols</b> is defined as follows in Dbghelp.h. 

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#if !defined(_IMAGEHLP_SOURCE_) &amp;&amp; defined(_IMAGEHLP64)
#define SymEnumerateSymbols SymEnumerateSymbols64
#define SymEnumerateSymbolsW SymEnumerateSymbolsW64
#else
BOOL
IMAGEAPI
SymEnumerateSymbols(
    __in HANDLE hProcess,
    __in ULONG BaseOfDll,
    __in PSYM_ENUMSYMBOLS_CALLBACK EnumSymbolsCallback,
    __in_opt PVOID UserContext
    );

BOOL
IMAGEAPI
SymEnumerateSymbolsW(
    __in HANDLE hProcess,
    __in ULONG BaseOfDll,
    __in PSYM_ENUMSYMBOLS_CALLBACKW EnumSymbolsCallback,
    __in_opt PVOID UserContext
    );
#endif</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/7b28f70b-2d97-4cc2-8064-dfb806f9cffa">DbgHelp Functions</a>



<a href="https://msdn.microsoft.com/e1232657-baf6-4e5b-9995-a382aa1391c2">SymEnumSymbols</a>



<a href="https://msdn.microsoft.com/e1430398-041f-4edd-b7b0-de3a60a42b37">SymEnumerateSymbolsProc64</a>



<a href="https://msdn.microsoft.com/fb1c98cb-6cd0-4218-aea4-384c24c66395">SymInitialize</a>
 

 

