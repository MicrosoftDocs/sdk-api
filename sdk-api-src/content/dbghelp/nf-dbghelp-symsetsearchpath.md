---
UID: NF:dbghelp.SymSetSearchPath
title: SymSetSearchPath function (dbghelp.h)
description: Sets the search path for the specified process.
helpviewer_keywords: ["SymSetSearchPath","SymSetSearchPath function","SymSetSearchPathW","_win32_symsetsearchpath","base.symsetsearchpath","dbghelp/SymSetSearchPath","dbghelp/SymSetSearchPathW"]
old-location: base\symsetsearchpath.htm
tech.root: Debug
ms.assetid: 564ba1f6-65c6-4c45-bdbf-41ef0dd8a39d
ms.date: 12/05/2018
ms.keywords: SymSetSearchPath, SymSetSearchPath function, SymSetSearchPathW, _win32_symsetsearchpath, base.symsetsearchpath, dbghelp/SymSetSearchPath, dbghelp/SymSetSearchPathW
req.header: dbghelp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SymSetSearchPathW (Unicode) and SymSetSearchPath (ANSI)
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
 - SymSetSearchPath
 - dbghelp/SymSetSearchPath
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
 - SymSetSearchPath
 - SymSetSearchPath
 - SymSetSearchPathW
---

# SymSetSearchPath function


## -description

Sets the search path for the specified process.

## -parameters

### -param hProcess [in]

A handle to the process that was originally passed to the 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-syminitialize">SymInitialize</a> function.

### -param SearchPath [in, optional]

The symbol search path. The string can contain multiple paths separated by semicolons.

## -returns

If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. To retrieve extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The symbol search path can be changed any number of times while the library is in use by an application. The change affects all future calls to the symbol handler.

To get the current search path, call the 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symgetsearchpath">SymGetSearchPath</a> function.

All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

To call the Unicode version of this function, define DBGHELP_TRANSLATE_TCHAR.

## -see-also

<a href="/windows/desktop/Debug/dbghelp-functions">DbgHelp Functions</a>



<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symgetsearchpath">SymGetSearchPath</a>



<a href="/windows/desktop/api/dbghelp/nf-dbghelp-syminitialize">SymInitialize</a>