---
UID: NF:dbghelp.SymGetTypeFromNameW
title: SymGetTypeFromNameW function
author: windows-sdk-content
description: Retrieves a type index for the specified type name.
old-location: base\symgettypefromname.htm
tech.root: debug
ms.assetid: 3a48365f-3b8a-493d-9fd9-dde77be9ced2
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: SymGetTypeFromName, SymGetTypeFromName function, SymGetTypeFromNameW, _win32_symgettypefromname, base.symgettypefromname, dbghelp/SymGetTypeFromName, dbghelp/SymGetTypeFromNameW
ms.topic: function
req.header: dbghelp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SymGetTypeFromNameW (Unicode) and SymGetTypeFromName (ANSI)
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
 - SymGetTypeFromName
 - SymGetTypeFromName
 - SymGetTypeFromNameW
product: Windows
targetos: Windows
req.typenames: 
req.redist: DbgHelp.dll 5.1 or later
---

# SymGetTypeFromNameW function


## -description


Retrieves a type index for the specified type name.


## -parameters




### -param hProcess [in]

A handle to a process. This handle must have been previously passed to the 
<a href="https://msdn.microsoft.com/fb1c98cb-6cd0-4218-aea4-384c24c66395">SymInitialize</a> function.


### -param BaseOfDll [in]

The base address of the module.


### -param Name [in]

The name of the type.


### -param Symbol [in, out]

A pointer to a 
<a href="https://msdn.microsoft.com/785a9702-8b77-4ce1-99df-143ce78490ab">SYMBOL_INFO</a> structure. The <b>TypeIndex</b> member contains the type index.


## -returns



If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. To retrieve extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



To retrieve information about the type, pass the type index to the 
<a href="https://msdn.microsoft.com/bc94a5b1-d49d-425a-89a8-c584c3979930">SymGetTypeInfo</a> function.

All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

To call the Unicode version of this function, define DBGHELP_TRANSLATE_TCHAR.




## -see-also




<a href="https://msdn.microsoft.com/7b28f70b-2d97-4cc2-8064-dfb806f9cffa">DbgHelp Functions</a>



<a href="https://msdn.microsoft.com/785a9702-8b77-4ce1-99df-143ce78490ab">SYMBOL_INFO</a>



<a href="https://msdn.microsoft.com/bc94a5b1-d49d-425a-89a8-c584c3979930">SymGetTypeInfo</a>
 

 

