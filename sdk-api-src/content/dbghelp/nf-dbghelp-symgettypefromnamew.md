---
UID: NF:dbghelp.SymGetTypeFromNameW
title: SymGetTypeFromNameW function (dbghelp.h)
author: windows-sdk-content
description: Retrieves a type index for the specified type name.
old-location: base\symgettypefromname.htm
tech.root: Debug
ms.assetid: 3a48365f-3b8a-493d-9fd9-dde77be9ced2
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: SymGetTypeFromName, SymGetTypeFromName function, SymGetTypeFromNameW, _win32_symgettypefromname, base.symgettypefromname, dbghelp/SymGetTypeFromName, dbghelp/SymGetTypeFromNameW
ms.topic: function
f1_keywords: 
 - "dbghelp/SymGetTypeFromName"
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
ms.custom: 19H1
---

# SymGetTypeFromNameW function


## -description


Retrieves a type index for the specified type name.


## -parameters




### -param hProcess [in]

A handle to a process. This handle must have been previously passed to the 
<a href="https://docs.microsoft.com/windows/desktop/api/dbghelp/nf-dbghelp-syminitialize">SymInitialize</a> function.


### -param BaseOfDll [in]

The base address of the module.


### -param Name [in]

The name of the type.


### -param Symbol [in, out]

A pointer to a 
<a href="https://docs.microsoft.com/windows/desktop/api/dbghelp/ns-dbghelp-_symbol_info">SYMBOL_INFO</a> structure. The <b>TypeIndex</b> member contains the type index.


## -returns



If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. To retrieve extended error information, call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



To retrieve information about the type, pass the type index to the 
<a href="https://docs.microsoft.com/windows/desktop/api/dbghelp/nf-dbghelp-symgettypeinfo">SymGetTypeInfo</a> function.

All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

To call the Unicode version of this function, define DBGHELP_TRANSLATE_TCHAR.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Debug/dbghelp-functions">DbgHelp Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dbghelp/ns-dbghelp-_symbol_info">SYMBOL_INFO</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dbghelp/nf-dbghelp-symgettypeinfo">SymGetTypeInfo</a>
 

 

