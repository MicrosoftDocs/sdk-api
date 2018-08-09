---
UID: NF:dbghelp.SymEnumTypesByName
title: SymEnumTypesByName function
author: windows-sdk-content
description: Enumerates all user-defined types.
old-location: base\symenumtypesbyname.htm
old-project: debug
ms.assetid: 48acb588-23fa-44f3-8b8c-f3c76371d1fd
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: SymEnumTypesByName, SymEnumTypesByName function, SymEnumTypesByNameW, base.symenumtypesbyname, dbghelp/SymEnumTypesByName, dbghelp/SymEnumTypesByNameW
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
req.unicode-ansi: SymEnumTypesByNameW (Unicode) and SymEnumTypesByName (ANSI)
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
 - imagehlp.dll
api_name:
 - SymEnumTypesByName
 - SymEnumTypesByName
 - SymEnumTypesByNameW
product: Windows
targetos: Windows
req.lib: Dbghelp.lib
req.dll: Dbghelp.dll
req.irql: 
---

# SymEnumTypesByName function


## -description


Enumerates all user-defined types.


## -parameters




### -param hProcess [in]

A handle to a process. This handle must have been previously passed to the 
<a href="https://msdn.microsoft.com/fb1c98cb-6cd0-4218-aea4-384c24c66395">SymInitialize</a> function.


### -param BaseOfDll [in]

The base address of the module.


### -param mask [in, optional]

A wildcard expression that indicates the names of the symbols to be enumerated. To specify a module name, use the !<i>mod</i> syntax.


### -param EnumSymbolsCallback [in]

A pointer to an 
<a href="https://msdn.microsoft.com/c9f9aad8-754d-4ec8-92a3-8cf1929b9d8a">SymEnumSymbolsProc</a> callback function that receives the symbol information.


### -param UserContext [in]

A user-defined value to be passed to the callback function, or <b>NULL</b>. This parameter is typically used by an application to pass a pointer to a data structure that provides context information for the callback function.


## -returns



If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. To retrieve extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

To call the Unicode version of this function, define DBGHELP_TRANSLATE_TCHAR.




## -see-also




<a href="https://msdn.microsoft.com/7b28f70b-2d97-4cc2-8064-dfb806f9cffa">DbgHelp Functions</a>



<a href="https://msdn.microsoft.com/c9f9aad8-754d-4ec8-92a3-8cf1929b9d8a">SymEnumSymbolsProc</a>
 

 

