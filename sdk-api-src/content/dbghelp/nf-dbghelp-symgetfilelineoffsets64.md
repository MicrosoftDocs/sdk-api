---
UID: NF:dbghelp.SymGetFileLineOffsets64
title: SymGetFileLineOffsets64 function
author: windows-sdk-content
description: Locates line information for the specified module and file name.
old-location: base\symgetfilelineoffsets64.htm
old-project: debug
ms.assetid: c83deef1-3476-4d06-a2e1-a3428c2f44d7
ms.author: windowssdkdev
ms.date: 05/18/2018
ms.keywords: SymGetFileLineOffsets64, SymGetFileLineOffsets64 function, base.symgetfilelineoffsets64, dbghelp/SymGetFileLineOffsets64
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
 - SymGetFileLineOffsets64
product: Windows
targetos: Windows
req.lib: Dbghelp.lib
req.dll: Dbghelp.dll
req.irql: 
---

# SymGetFileLineOffsets64 function


## -description


Locates line information for the specified module and file name.


## -parameters




### -param hProcess [in]

A handle to the process that was originally passed to the 
<a href="https://msdn.microsoft.com/fb1c98cb-6cd0-4218-aea4-384c24c66395">SymInitialize</a> function.


### -param ModuleName [in, optional]

The name of the module in which  lines are to be located. If this parameter is <b>NULL</b>, the function searches all modules.


### -param FileName [in]

The name of the file in which lines are to be located.


### -param Buffer [out]

An array of offsets for each line. The offset for the line n is stored in element n-1. Array elements for lines that do not have line information are left unchanged.


### -param BufferLines [in]

The size of the <i>Buffer</i> array, in elements.


## -returns




						If the function succeeds, the return value is the highest line number found.
						This value is zero if no line information was found.

If the function fails, the return value is LINE_ERROR. To retrieve extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.




## -see-also




<a href="https://msdn.microsoft.com/7b28f70b-2d97-4cc2-8064-dfb806f9cffa">DbgHelp Functions</a>
 

 

