---
UID: NF:dbghelp.SymGetSourceFileW
title: SymGetSourceFileW function
author: windows-sdk-content
description: Retrieves the specified source file from the source server.
old-location: base\symgetsourcefile.htm
tech.root: debug
ms.assetid: 1d2115fb-2725-4fae-abb7-ff1b8a802c69
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: SymGetSourceFile, SymGetSourceFile function, SymGetSourceFileW, base.symgetsourcefile, dbghelp/SymGetSourceFile, dbghelp/SymGetSourceFileW
ms.topic: function
req.header: dbghelp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SymGetSourceFileW (Unicode) and SymGetSourceFile (ANSI)
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
 - SymGetSourceFile
 - SymGetSourceFile
 - SymGetSourceFileW
product: Windows
targetos: Windows
req.typenames: 
req.redist: DbgHelp.dll 6.2 or later
---

# SymGetSourceFileW function


## -description


Retrieves the specified source file from the source server.


## -parameters




### -param hProcess [in]

A handle to a process. This handle must have been previously passed to the 
<a href="https://msdn.microsoft.com/fb1c98cb-6cd0-4218-aea4-384c24c66395">SymInitialize</a> function.


### -param Base [in]

The base address of the module. 


### -param Params [in, optional]

This parameter is unused.


### -param FileSpec [in]

The name of the source file.


### -param FilePath [out]

A pointer to a 
buffer that receives the fully qualified path of the source file.


### -param Size [in]

The size of the <i>FilePath</i> buffer, in characters.


## -returns



If the function succeeds, the return value is <b>TRUE</b>.
						

If the function fails, the return value is <b>FALSE</b>. To retrieve extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



To control which directory receives the source files, use the <a href="https://msdn.microsoft.com/12e65054-c4d5-44b9-8597-b841cac012f5">SymSetHomeDirectory</a> function.

All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

To call the Unicode version of this function, define DBGHELP_TRANSLATE_TCHAR.




## -see-also




<a href="https://msdn.microsoft.com/7b28f70b-2d97-4cc2-8064-dfb806f9cffa">DbgHelp Functions</a>



<a href="https://msdn.microsoft.com/c7bf51ce-7fb4-49aa-ad33-e551b2c8362b">Source Server</a>
 

 

