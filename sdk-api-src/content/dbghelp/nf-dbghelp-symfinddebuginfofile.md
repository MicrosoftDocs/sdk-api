---
UID: NF:dbghelp.SymFindDebugInfoFile
title: SymFindDebugInfoFile function (dbghelp.h)
description: The SymFindDebugInfoFile function (dbghelp.h) locates a .dbg file in the process search path.
helpviewer_keywords: ["SymFindDebugInfoFile","SymFindDebugInfoFile function","SymFindDebugInfoFileW","base.symfinddebuginfofile","dbghelp/SymFindDebugInfoFile","dbghelp/SymFindDebugInfoFileW"]
old-location: base\symfinddebuginfofile.htm
tech.root: Debug
ms.assetid: ea4879b2-edf8-4542-b16a-41777c0068cd
ms.date: 08/04/2022
ms.keywords: SymFindDebugInfoFile, SymFindDebugInfoFile function, SymFindDebugInfoFileW, base.symfinddebuginfofile, dbghelp/SymFindDebugInfoFile, dbghelp/SymFindDebugInfoFileW
req.header: dbghelp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SymFindDebugInfoFileW (Unicode) and SymFindDebugInfoFile (ANSI)
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
req.redist: DbgHelp.dll 6.6 or later
ms.custom: 19H1
f1_keywords:
 - SymFindDebugInfoFile
 - dbghelp/SymFindDebugInfoFile
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
 - SymFindDebugInfoFile
 - SymFindDebugInfoFile
 - SymFindDebugInfoFileW
---

# SymFindDebugInfoFile function


## -description

Locates a .dbg file in the process search path.

## -parameters

### -param hProcess [in]

A handle to the process that was originally passed to the 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-syminitialize">SymInitialize</a> function.

### -param FileName [in]

The name of the .dbg file. You can use a partial path.

### -param DebugFilePath [out]

The fully qualified path of the .dbg file. This buffer must be at least MAX_PATH characters.

### -param Callback [in, optional]

An application-defined callback function that verifies whether the correct file was found or the function should continue its search. For more information, see 
<a href="/windows/desktop/api/dbghelp/nc-dbghelp-pfind_debug_file_callback">FindDebugInfoFileProc</a>. 




This parameter can be <b>NULL</b>.

### -param CallerData [in, optional]

A user-defined value or <b>NULL</b>. This value is simply passed to the callback function. This parameter is typically used by an application to pass a pointer to a data structure that provides some context for the callback function.

## -returns

If the function succeeds, the return value is an open handle to the .dbg file.

If the function fails, the return value is <b>NULL</b>. To retrieve extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

This function uses the search path set using the 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-syminitialize">SymInitialize</a> or <a href="/windows/desktop/api/dbghelp/nf-dbghelp-symsetsearchpath">SymSetSearchPath</a> function.

All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

To call the Unicode version of this function, define DBGHELP_TRANSLATE_TCHAR.

## -see-also

<a href="/windows/desktop/Debug/dbghelp-functions">DbgHelp Functions</a>



<a href="/windows/desktop/api/dbghelp/nc-dbghelp-pfind_debug_file_callback">FindDebugInfoFileProc</a>
