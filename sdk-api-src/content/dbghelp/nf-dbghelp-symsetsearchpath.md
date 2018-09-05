---
UID: NF:dbghelp.SymSetSearchPath
title: SymSetSearchPath function
author: windows-sdk-content
description: Sets the search path for the specified process.
old-location: base\symsetsearchpath.htm
old-project: debug
ms.assetid: 564ba1f6-65c6-4c45-bdbf-41ef0dd8a39d
ms.author: windowssdkdev
ms.date: 08/28/2018
ms.keywords: SymSetSearchPath, SymSetSearchPath function, SymSetSearchPathW, _win32_symsetsearchpath, base.symsetsearchpath, dbghelp/SymSetSearchPath, dbghelp/SymSetSearchPathW
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
req.unicode-ansi: SymSetSearchPathW (Unicode) and SymSetSearchPath (ANSI)
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
 - SymSetSearchPath
 - SymSetSearchPath
 - SymSetSearchPathW
product: Windows
targetos: Windows
req.lib: Dbghelp.lib
req.dll: Dbghelp.dll
req.irql: 
---

# SymSetSearchPath function


## -description


Sets the search path for the specified process.


## -parameters




### -param hProcess [in]

A handle to the process that was originally passed to the 
<a href="https://msdn.microsoft.com/fb1c98cb-6cd0-4218-aea4-384c24c66395">SymInitialize</a> function.


### -param SearchPath [in, optional]

The symbol search path. The string can contain multiple paths separated by semicolons.


## -returns



If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. To retrieve extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The symbol search path can be changed any number of times while the library is in use by an application. The change affects all future calls to the symbol handler.

To get the current search path, call the 
<a href="https://msdn.microsoft.com/aa8c8450-ee67-4614-98a1-5feebdd3a788">SymGetSearchPath</a> function.

All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

To call the Unicode version of this function, define DBGHELP_TRANSLATE_TCHAR.




## -see-also




<a href="https://msdn.microsoft.com/7b28f70b-2d97-4cc2-8064-dfb806f9cffa">DbgHelp Functions</a>



<a href="https://msdn.microsoft.com/aa8c8450-ee67-4614-98a1-5feebdd3a788">SymGetSearchPath</a>



<a href="https://msdn.microsoft.com/fb1c98cb-6cd0-4218-aea4-384c24c66395">SymInitialize</a>
 

 

