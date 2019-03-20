---
UID: NF:dbghelp.SymEnumLines
title: SymEnumLines function (dbghelp.h)
author: windows-sdk-content
description: Enumerates all lines in the specified module.
old-location: base\symenumlines.htm
tech.root: Debug
ms.assetid: d518b320-e4db-4bd1-8221-583eb84c292c
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: SymEnumLines, SymEnumLines function, SymEnumLinesW, base.symenumlines, dbghelp/SymEnumLines, dbghelp/SymEnumLinesW
ms.topic: function
req.header: dbghelp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SymEnumLinesW (Unicode) and SymEnumLines (ANSI)
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
 - SymEnumLines
 - SymEnumLines
 - SymEnumLinesW
product: Windows
targetos: Windows
req.typenames: 
req.redist: DbgHelp.dll 6.1 or later
---

# SymEnumLines function


## -description


Enumerates all lines in the specified module.


## -parameters




### -param hProcess [in]

A handle to a process. This handle must have been previously passed to the 
<a href="https://msdn.microsoft.com/fb1c98cb-6cd0-4218-aea4-384c24c66395">SymInitialize</a> function.


### -param Base [in]

The base address of the module. 


### -param Obj [in, optional]

The name of an .obj file within the module. The scope of the enumeration is limited to this file. If this parameter is <b>NULL</b> or an empty string, all .obj files are searched. 


### -param File [in, optional]

A wildcard expression that indicates the names of the source files to be searched. If this parameter is <b>NULL</b> or an empty string, all files are searched.


### -param EnumLinesCallback [in]

A 
<a href="https://msdn.microsoft.com/7379dd04-72a4-45b6-b02a-d3e8a5aaf0d7">SymEnumLinesProc</a> callback function that receives the line information.


### -param UserContext [in, optional]

A user-defined value that is passed to the callback function, or <b>NULL</b>. This parameter is typically used by an application to pass a pointer to a data structure that provides context for the callback function.


## -returns



If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. To retrieve extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



This function is supported for PDB information only. If you have COFF information, try using one of the <b>SymGetLineXXX</b> functions.

All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

To call the Unicode version of this function, define DBGHELP_TRANSLATE_TCHAR.




## -see-also




<a href="https://msdn.microsoft.com/7b28f70b-2d97-4cc2-8064-dfb806f9cffa">DbgHelp Functions</a>



<a href="https://msdn.microsoft.com/c9f9aad8-754d-4ec8-92a3-8cf1929b9d8a">SymEnumLinesProc</a>
 

 

