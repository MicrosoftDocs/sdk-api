---
UID: NF:dbghelp.SymGetScopeW
title: SymGetScopeW function (dbghelp.h)
author: windows-sdk-content
description: Retrieves the scope for the specified index.
old-location: base\symgetscope.htm
tech.root: Debug
ms.assetid: 048a4d07-bf87-4dbc-9169-d8782040b205
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: SymGetScope, SymGetScope function, SymGetScopeW, base.symgetscope, dbghelp/SymGetScope, dbghelp/SymGetScopeW
ms.topic: function
req.header: dbghelp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SymGetScopeW (Unicode) and SymGetScope (ANSI)
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
 - SymGetScope
 - SymGetScope
 - SymGetScopeW
product: Windows
targetos: Windows
req.typenames: 
req.redist: DbgHelp.dll 6.2 or later
---

# SymGetScopeW function


## -description


Retrieves the scope for the specified index.


## -parameters




### -param hProcess [in]

A handle to a process. This handle must have been previously passed to the 
<a href="https://msdn.microsoft.com/fb1c98cb-6cd0-4218-aea4-384c24c66395">SymInitialize</a> function.


### -param BaseOfDll [in]

The base address of the module.


### -param Index [in]

A unique value for the symbol.


### -param Symbol [in, out]

A pointer to a 
<a href="https://msdn.microsoft.com/785a9702-8b77-4ce1-99df-143ce78490ab">SYMBOL_INFO</a> structure. The <b>Scope</b> member contains the scope.


## -returns



If the function succeeds, the return value is <b>TRUE</b>.
						

If the function fails, the return value is <b>FALSE</b>. To retrieve extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.




## -see-also




<a href="https://msdn.microsoft.com/7b28f70b-2d97-4cc2-8064-dfb806f9cffa">DbgHelp Functions</a>



<a href="https://msdn.microsoft.com/785a9702-8b77-4ce1-99df-143ce78490ab">SYMBOL_INFO</a>



<a href="https://msdn.microsoft.com/7f7bcf12-8d8d-4dea-8191-4f7b24be1b5a">SymSetScopeFromAddr</a>



<a href="https://msdn.microsoft.com/06792478-35e2-4f05-85c9-910909fe65cd">SymSetScopeFromIndex</a>
 

 

