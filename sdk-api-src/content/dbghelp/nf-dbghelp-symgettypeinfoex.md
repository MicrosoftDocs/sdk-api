---
UID: NF:dbghelp.SymGetTypeInfoEx
title: SymGetTypeInfoEx function (dbghelp.h)
description: Retrieves multiple pieces of type information.
helpviewer_keywords: ["SymGetTypeInfoEx","SymGetTypeInfoEx function","base.symgettypeinfoex","dbghelp/SymGetTypeInfoEx"]
old-location: base\symgettypeinfoex.htm
tech.root: Debug
ms.assetid: 77e0a8ad-8c75-4bb2-869a-670429475ccc
ms.date: 12/05/2018
ms.keywords: SymGetTypeInfoEx, SymGetTypeInfoEx function, base.symgettypeinfoex, dbghelp/SymGetTypeInfoEx
req.header: dbghelp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dbghelp.lib
req.dll: Dbghelp.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: DbgHelp.dll 6.3 or later
ms.custom: 19H1
f1_keywords:
 - SymGetTypeInfoEx
 - dbghelp/SymGetTypeInfoEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Dbghelp.dll
api_name:
 - SymGetTypeInfoEx
---

# SymGetTypeInfoEx function


## -description

Retrieves multiple pieces of type information.

## -parameters

### -param hProcess [in]

A handle to a process. This handle must have been previously passed to the 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-syminitialize">SymInitialize</a> function.

### -param ModBase [in]

The base address of the module.

### -param Params [in, out]

A pointer to an <a href="/windows/desktop/api/dbghelp/ns-dbghelp-imagehlp_get_type_info_params">IMAGEHLP_GET_TYPE_INFO_PARAMS</a> structure that specifies input and output information for the query.

## -returns

If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. To retrieve extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

## -see-also

<a href="/windows/desktop/Debug/dbghelp-functions">DbgHelp Functions</a>



<a href="/windows/desktop/api/dbghelp/ns-dbghelp-imagehlp_get_type_info_params">IMAGEHLP_GET_TYPE_INFO_PARAMS</a>



<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symgettypefromname">SymGetTypeFromName</a>