---
UID: NF:dbghelp.SymFromName
title: SymFromName function
author: windows-sdk-content
description: Retrieves symbol information for the specified name.
old-location: base\symfromname.htm
tech.root: debug
ms.assetid: 26b9eba7-2038-4640-aeb2-3052889b14ea
ms.author: windowssdkdev
ms.date: 11/13/2018
ms.keywords: SymFromName, SymFromName function, SymFromNameW, _win32_symfromname, base.symfromname, dbghelp/SymFromName, dbghelp/SymFromNameW
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
req.unicode-ansi: SymFromNameW (Unicode) and SymFromName (ANSI)
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
 - SymFromName
 - SymFromName
 - SymFromNameW
product: Windows
targetos: Windows
req.typenames: 
req.redist: DbgHelp.dll 5.1 or later
- apiref
: 
- 
: 
- SymFromName
: 
---

# SymFromName function


## -description


Retrieves symbol information for the specified name.


## -parameters




### -param hProcess [in]

A handle to a process. This handle must have been previously passed to the 
<a href="https://msdn.microsoft.com/fb1c98cb-6cd0-4218-aea4-384c24c66395">SymInitialize</a> function.


### -param Name [in]

The name of the symbol to be located.


### -param Symbol [in, out]

A pointer to a 
<a href="https://msdn.microsoft.com/785a9702-8b77-4ce1-99df-143ce78490ab">SYMBOL_INFO</a> structure that provides information about the symbol.


## -returns



If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. To retrieve extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

To call the Unicode version of this function, define DBGHELP_TRANSLATE_TCHAR.


#### Examples

For an example, see 
<a href="https://msdn.microsoft.com/d3a9d73e-fb77-4be3-a881-c258bcc587fe">Retrieving Symbol Information by Name</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/7b28f70b-2d97-4cc2-8064-dfb806f9cffa">DbgHelp Functions</a>



<a href="https://msdn.microsoft.com/785a9702-8b77-4ce1-99df-143ce78490ab">SYMBOL_INFO</a>
 

 

