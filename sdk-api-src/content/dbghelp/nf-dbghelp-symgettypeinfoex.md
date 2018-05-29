---
UID: NF:dbghelp.SymGetTypeInfoEx
title: SymGetTypeInfoEx function
author: windows-sdk-content
description: Retrieves multiple pieces of type information.
old-location: base\symgettypeinfoex.htm
old-project: Debug
ms.assetid: 77e0a8ad-8c75-4bb2-869a-670429475ccc
ms.author: windowssdkdev
ms.date: 05/17/2018
ms.keywords: SymGetTypeInfoEx, SymGetTypeInfoEx function, base.symgettypeinfoex, dbghelp/SymGetTypeInfoEx
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
req.typenames: IMAGEHLP_SYMBOL_TYPE_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Dbghelp.dll
api_name:
-	SymGetTypeInfoEx
product: Windows
targetos: Windows
req.lib: Dbghelp.lib
req.dll: Dbghelp.dll
req.irql: 
---

# SymGetTypeInfoEx function


## -description


Retrieves multiple pieces of type information.


## -parameters




### -param hProcess [in]

A handle to a process. This handle must have been previously passed to the 
<a href="https://msdn.microsoft.com/fb1c98cb-6cd0-4218-aea4-384c24c66395">SymInitialize</a> function.


### -param ModBase [in]

The base address of the module.


### -param Params [in, out]

A pointer to an <a href="https://msdn.microsoft.com/f3885945-9a96-49d9-a535-7b37220e1da4">IMAGEHLP_GET_TYPE_INFO_PARAMS</a> structure that specifies input and output information for the query.


## -returns



If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. To retrieve extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.




## -see-also




<a href="https://msdn.microsoft.com/7b28f70b-2d97-4cc2-8064-dfb806f9cffa">DbgHelp Functions</a>



<a href="https://msdn.microsoft.com/f3885945-9a96-49d9-a535-7b37220e1da4">IMAGEHLP_GET_TYPE_INFO_PARAMS</a>



<a href="https://msdn.microsoft.com/3a48365f-3b8a-493d-9fd9-dde77be9ced2">SymGetTypeFromName</a>
 

 

