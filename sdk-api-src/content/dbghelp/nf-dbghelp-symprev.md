---
UID: NF:dbghelp.SymPrev
title: SymPrev function
author: windows-sdk-content
description: Retrieves symbol information for the previous symbol.
old-location: base\symprev.htm
old-project: Debug
ms.assetid: 45503f0c-cb66-4ddf-986d-02de7fc480f2
ms.author: windowssdkdev
ms.date: 05/17/2018
ms.keywords: SymPrev, SymPrev function, SymPrevW, base.symprev, dbghelp/SymPrev, dbghelp/SymPrevW
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
req.unicode-ansi: SymPrevW (Unicode) and SymPrev (ANSI)
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
 - SymPrev
 - SymPrev
 - SymPrevW
product: Windows
targetos: Windows
req.lib: Dbghelp.lib
req.dll: Dbghelp.dll
req.irql: 
---

# SymPrev function


## -description


Retrieves symbol information for the previous symbol.


## -parameters




### -param hProcess [in]

A handle to a process. This handle must have been previously passed to the 
<a href="https://msdn.microsoft.com/fb1c98cb-6cd0-4218-aea4-384c24c66395">SymInitialize</a> function.


### -param si

TBD




#### - Symbol [in, out]

A pointer to a 
<a href="https://msdn.microsoft.com/785a9702-8b77-4ce1-99df-143ce78490ab">SYMBOL_INFO</a> structure that provides information about the current symbol. Upon return, the structure contains information about the previous symbol.


## -returns




						If the function succeeds, the return value is <b>TRUE</b>.
						

If the function fails, the return value is <b>FALSE</b>. To retrieve extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



This function requires that the <a href="https://msdn.microsoft.com/785a9702-8b77-4ce1-99df-143ce78490ab">SYMBOL_INFO</a> structure have valid data for the current symbol. The previous symbol is the symbol with a virtual address that immediately precedes this symbol.

All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

To call the Unicode version of this function, define DBGHELP_TRANSLATE_TCHAR.




## -see-also




<a href="https://msdn.microsoft.com/7b28f70b-2d97-4cc2-8064-dfb806f9cffa">DbgHelp Functions</a>



<a href="https://msdn.microsoft.com/785a9702-8b77-4ce1-99df-143ce78490ab">SYMBOL_INFO</a>



<a href="https://msdn.microsoft.com/ffd2d416-7149-4a4c-a1d5-7a7f3bdf5dc4">SymNext</a>
 

 

