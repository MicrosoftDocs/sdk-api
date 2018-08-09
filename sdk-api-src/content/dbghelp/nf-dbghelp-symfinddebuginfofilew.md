---
UID: NF:dbghelp.SymFindDebugInfoFileW
title: SymFindDebugInfoFileW function
author: windows-sdk-content
description: Locates a .dbg file in the process search path.
old-location: base\symfinddebuginfofile.htm
old-project: debug
ms.assetid: ea4879b2-edf8-4542-b16a-41777c0068cd
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: SymFindDebugInfoFile, SymFindDebugInfoFile function, SymFindDebugInfoFileW, base.symfinddebuginfofile, dbghelp/SymFindDebugInfoFile, dbghelp/SymFindDebugInfoFileW
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
req.unicode-ansi: SymFindDebugInfoFileW (Unicode) and SymFindDebugInfoFile (ANSI)
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
 - SymFindDebugInfoFile
 - SymFindDebugInfoFile
 - SymFindDebugInfoFileW
product: Windows
targetos: Windows
req.lib: Dbghelp.lib
req.dll: Dbghelp.dll
req.irql: 
---

# SymFindDebugInfoFileW function


## -description


Locates a .dbg file in the process search path.


## -parameters




### -param hProcess [in]

A handle to the process that was originally passed to the 
<a href="https://msdn.microsoft.com/fb1c98cb-6cd0-4218-aea4-384c24c66395">SymInitialize</a> function.


### -param FileName [in]

The name of the .dbg file. You can use a partial path.


### -param DebugFilePath [out]

The fully qualified path of the .dbg file. This buffer must be at least MAX_PATH characters.


### -param Callback [in, optional]

An application-defined callback function that verifies whether the correct file was found or the function should continue its search. For more information, see 
<a href="https://msdn.microsoft.com/c7ccc66a-7897-4430-8874-a4ba66a5cce7">FindDebugInfoFileProc</a>. 




This parameter can be <b>NULL</b>.


### -param CallerData [in, optional]

A user-defined value or <b>NULL</b>. This value is simply passed to the callback function. This parameter is typically used by an application to pass a pointer to a data structure that provides some context for the callback function.


## -returns



If the function succeeds, the return value is an open handle to the .dbg file.

If the function fails, the return value is <b>NULL</b>. To retrieve extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



This function uses the search path set using the 
<a href="https://msdn.microsoft.com/fb1c98cb-6cd0-4218-aea4-384c24c66395">SymInitialize</a> or <a href="https://msdn.microsoft.com/564ba1f6-65c6-4c45-bdbf-41ef0dd8a39d">SymSetSearchPath</a> function.

All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

To call the Unicode version of this function, define DBGHELP_TRANSLATE_TCHAR.




## -see-also




<a href="https://msdn.microsoft.com/7b28f70b-2d97-4cc2-8064-dfb806f9cffa">DbgHelp Functions</a>



<a href="https://msdn.microsoft.com/c7ccc66a-7897-4430-8874-a4ba66a5cce7">FindDebugInfoFileProc</a>
 

 

