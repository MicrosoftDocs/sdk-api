---
UID: NF:dbghelp.SymEnumSourceFiles
title: SymEnumSourceFiles function
author: windows-sdk-content
description: Enumerates all source files in a process.
old-location: base\symenumsourcefiles.htm
tech.root: debug
ms.assetid: 4649bdc6-74c5-4529-bedc-64e0277144d0
ms.author: windowssdkdev
ms.date: 08/28/2018
ms.keywords: SymEnumSourceFiles, SymEnumSourceFiles function, SymEnumSourceFilesW, base.symenumsourcefiles, dbghelp/SymEnumSourceFiles, dbghelp/SymEnumSourceFilesW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: dbghelp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SymEnumSourceFilesW (Unicode) and SymEnumSourceFiles (ANSI)
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
 - SymEnumSourceFiles
 - SymEnumSourceFiles
 - SymEnumSourceFilesW
product: Windows
targetos: Windows
req.typenames: 
req.redist: DbgHelp.dll 6.2 or later
---

# SymEnumSourceFiles function


## -description


Enumerates all source files in a process.


## -parameters




### -param hProcess [in]

A handle to a process. This handle must have been previously passed to the 
<a href="https://msdn.microsoft.com/fb1c98cb-6cd0-4218-aea4-384c24c66395">SymInitialize</a> function.


### -param ModBase [in]

The base address of the module. If this value is zero and <i>Mask</i> contains an exclamation point (!), the function looks across modules. If this value is zero and <i>Mask</i> does not contain an exclamation point, the function uses the scope established by the 
<a href="https://msdn.microsoft.com/0a9c6bfe-5e60-48c4-af98-b910df3032d5">SymSetContext</a> function.


### -param Mask [in, optional]

A wildcard expression that indicates the names of the source files to be enumerated. To specify a module name, use the !<i>mod</i> syntax.

If this parameter is <b>NULL</b>, the function will enumerate all files.


### -param cbSrcFiles [in]

Pointer to a 
<a href="https://msdn.microsoft.com/b1d1e967-514d-43da-b470-23228fa03dd9">SymEnumSourceFilesProc</a> callback function that receives the source file information.


### -param UserContext [in, optional]

User-defined value that is passed to the callback function, or <b>NULL</b>. This parameter is typically used by an application to pass a pointer to a data structure that provides context for the callback function.


## -returns



If the function succeeds, the return value is <b>TRUE</b>.
						

If the function fails, the return value is <b>FALSE</b>. To retrieve extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.




## -see-also




<a href="https://msdn.microsoft.com/7b28f70b-2d97-4cc2-8064-dfb806f9cffa">DbgHelp Functions</a>



<a href="https://msdn.microsoft.com/b1d1e967-514d-43da-b470-23228fa03dd9">SymEnumSourceFilesProc</a>
 

 

