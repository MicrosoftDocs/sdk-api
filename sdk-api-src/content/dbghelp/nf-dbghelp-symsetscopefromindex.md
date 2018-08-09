---
UID: NF:dbghelp.SymSetScopeFromIndex
title: SymSetScopeFromIndex function
author: windows-sdk-content
description: Sets the local scope to the symbol that matches the specified index.
old-location: base\symsetscopefromindex.htm
old-project: debug
ms.assetid: 06792478-35e2-4f05-85c9-910909fe65cd
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: SymSetScopeFromIndex, SymSetScopeFromIndex function, base.symsetscopefromindex, dbghelp/SymSetScopeFromIndex
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
 - SymSetScopeFromIndex
product: Windows
targetos: Windows
req.lib: Dbghelp.lib
req.dll: Dbghelp.dll
req.irql: 
---

# SymSetScopeFromIndex function


## -description


Sets the local scope to the symbol that matches the specified index.


## -parameters




### -param hProcess [in]

A handle to a process. This handle must have been previously passed to the 
<a href="https://msdn.microsoft.com/fb1c98cb-6cd0-4218-aea4-384c24c66395">SymInitialize</a> function.


### -param BaseOfDll [in]

The base address of the module.


### -param Index [in]

The unique value for the symbol.


## -returns



If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. To retrieve extended error 
       information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.




## -see-also




<a href="https://msdn.microsoft.com/048a4d07-bf87-4dbc-9169-d8782040b205">SymGetScope</a>



<a href="https://msdn.microsoft.com/7f7bcf12-8d8d-4dea-8191-4f7b24be1b5a">SymSetScopeFromAddr</a>
 

 

