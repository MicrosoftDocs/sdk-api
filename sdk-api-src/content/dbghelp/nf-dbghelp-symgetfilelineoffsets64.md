---
UID: NF:dbghelp.SymGetFileLineOffsets64
title: SymGetFileLineOffsets64 function (dbghelp.h)
description: Locates line information for the specified module and file name.
helpviewer_keywords: ["SymGetFileLineOffsets64","SymGetFileLineOffsets64 function","base.symgetfilelineoffsets64","dbghelp/SymGetFileLineOffsets64"]
old-location: base\symgetfilelineoffsets64.htm
tech.root: Debug
ms.assetid: c83deef1-3476-4d06-a2e1-a3428c2f44d7
ms.date: 12/05/2018
ms.keywords: SymGetFileLineOffsets64, SymGetFileLineOffsets64 function, base.symgetfilelineoffsets64, dbghelp/SymGetFileLineOffsets64
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
 - SymGetFileLineOffsets64
 - dbghelp/SymGetFileLineOffsets64
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
 - SymGetFileLineOffsets64
---

# SymGetFileLineOffsets64 function


## -description

Locates line information for the specified module and file name.

## -parameters

### -param hProcess [in]

A handle to the process that was originally passed to the 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-syminitialize">SymInitialize</a> function.

### -param ModuleName [in, optional]

The name of the module in which  lines are to be located. If this parameter is <b>NULL</b>, the function searches all modules.

### -param FileName [in]

The name of the file in which lines are to be located.

### -param Buffer [out]

An array of offsets for each line. The offset for the line n is stored in element n-1. Array elements for lines that do not have line information are left unchanged.

### -param BufferLines [in]

The size of the <i>Buffer</i> array, in elements.

## -returns

If the function succeeds, the return value is the highest line number found.
						This value is zero if no line information was found.

If the function fails, the return value is LINE_ERROR. To retrieve extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

## -see-also

<a href="/windows/desktop/Debug/dbghelp-functions">DbgHelp Functions</a>