---
UID: NF:dbghelp.SymGetTypeInfo
title: SymGetTypeInfo function (dbghelp.h)
description: Retrieves type information for the specified type index.
helpviewer_keywords: ["SymGetTypeInfo","SymGetTypeInfo function","_win32_symgettypeinfo","base.symgettypeinfo","dbghelp/SymGetTypeInfo"]
old-location: base\symgettypeinfo.htm
tech.root: Debug
ms.assetid: bc94a5b1-d49d-425a-89a8-c584c3979930
ms.date: 12/05/2018
ms.keywords: SymGetTypeInfo, SymGetTypeInfo function, _win32_symgettypeinfo, base.symgettypeinfo, dbghelp/SymGetTypeInfo
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
req.redist: DbgHelp.dll 5.1 or later
ms.custom: 19H1
f1_keywords:
 - SymGetTypeInfo
 - dbghelp/SymGetTypeInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Dbghelp.dll
 - imagehlp.dll
api_name:
 - SymGetTypeInfo
---

# SymGetTypeInfo function


## -description

Retrieves type information for the specified type index. For larger queries, use the <a href="/windows/desktop/api/dbghelp/nf-dbghelp-symgettypeinfoex">SymGetTypeInfoEx</a> function.

## -parameters

### -param hProcess [in]

A handle to a process. This handle must have been previously passed to the 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-syminitialize">SymInitialize</a> function.

### -param ModBase [in]

The base address of the module.

### -param TypeId [in]

The type index. (A number of functions return a type index in the <b>TypeIndex</b> member of the 
<a href="/windows/desktop/api/dbghelp/ns-dbghelp-symbol_info">SYMBOL_INFO</a> structure.)

### -param GetType [in]

The information type. This parameter can be one of more of the values from the <a href="/windows/desktop/api/dbghelp/ne-dbghelp-imagehlp_symbol_type_info">IMAGEHLP_SYMBOL_TYPE_INFO</a> enumeration type.

### -param pInfo [out]

The data. The format of the data depends on the value of the <i>GetType</i> parameter.

## -returns

If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. To retrieve extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

For more details on the type information, see the documentation for the PDB format.

All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

## -see-also

<a href="/windows/desktop/Debug/dbghelp-functions">DbgHelp Functions</a>



<a href="/windows/desktop/api/dbghelp/ne-dbghelp-imagehlp_symbol_type_info">IMAGEHLP_SYMBOL_TYPE_INFO</a>



<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symgettypefromname">SymGetTypeFromName</a>



<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symgettypeinfoex">SymGetTypeInfoEx</a>