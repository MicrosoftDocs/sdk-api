---
UID: NF:dbghelp.SymFindExecutableImage
title: SymFindExecutableImage function
author: windows-sdk-content
description: Locates an executable file in the process search path.
old-location: base\symfindexecutableimage.htm
old-project: debug
ms.assetid: e81ff4bd-b9a0-4c90-86cb-67e721e2fd1b
ms.author: windowssdkdev
ms.date: 08/28/2018
ms.keywords: SymFindExecutableImage, SymFindExecutableImage function, SymFindExecutableImageW, base.symfindexecutableimage, dbghelp/SymFindExecutableImage, dbghelp/SymFindExecutableImageW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: dbghelp.h
req.include-header: 
req.redist: DbgHelp.dll 6.6 or later
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SymFindExecutableImageW (Unicode) and SymFindExecutableImage (ANSI)
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
 - SymFindExecutableImage
 - SymFindExecutableImage
 - SymFindExecutableImageW
product: Windows
targetos: Windows
req.lib: Dbghelp.lib
req.dll: Dbghelp.dll
req.irql: 
---

# SymFindExecutableImage function


## -description


Locates an executable file in the process search path.


## -parameters




### -param hProcess [in]

A handle to the process that was originally passed to the 
<a href="https://msdn.microsoft.com/fb1c98cb-6cd0-4218-aea4-384c24c66395">SymInitialize</a> function.


### -param FileName [in]

The name of the executable file. You can use a partial path.


### -param ImageFilePath [out]

The fully qualified path of the executable file. This buffer must be at least MAX_PATH characters.


### -param Callback [in]

An application-defined callback function that verifies whether the correct executable file was found, or whether the function should continue its search. For more information, see 
<a href="https://msdn.microsoft.com/cbd8cd63-8fdb-4314-8737-9f934de74f89">FindExecutableImageProc</a>. 




This parameter can be <b>NULL</b>.


### -param CallerData [in]

A user-defined value or <b>NULL</b>. This value is simply passed to the callback function. This parameter is typically used by an application to pass a pointer to a data structure that provides some context for the callback function.


## -returns



If the function succeeds, the return value is an open handle to the executable file.

If the function fails, the return value is <b>NULL</b>. To retrieve extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



This function uses the search path set using the 
<a href="https://msdn.microsoft.com/fb1c98cb-6cd0-4218-aea4-384c24c66395">SymInitialize</a> or <a href="https://msdn.microsoft.com/564ba1f6-65c6-4c45-bdbf-41ef0dd8a39d">SymSetSearchPath</a> function.

All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

To call the Unicode version of this function, define DBGHELP_TRANSLATE_TCHAR.




## -see-also




<a href="https://msdn.microsoft.com/7b28f70b-2d97-4cc2-8064-dfb806f9cffa">DbgHelp Functions</a>



<a href="https://msdn.microsoft.com/cbd8cd63-8fdb-4314-8737-9f934de74f89">FindExecutableImageProc</a>
 

 

