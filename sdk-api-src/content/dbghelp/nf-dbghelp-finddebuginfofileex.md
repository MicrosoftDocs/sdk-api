---
UID: NF:dbghelp.FindDebugInfoFileEx
title: FindDebugInfoFileEx function (dbghelp.h)
description: The FindDebugInfoFileEx function (dbghelp.h) locates the specified debug (.dbg) file.
helpviewer_keywords: ["FindDebugInfoFileEx","FindDebugInfoFileEx function","FindDebugInfoFileExW","_win32_finddebuginfofileex","base.finddebuginfofileex","dbghelp/FindDebugInfoFileEx","dbghelp/FindDebugInfoFileExW"]
old-location: base\finddebuginfofileex.htm
tech.root: Debug
ms.assetid: 1e89fe9a-4631-42b9-96ee-90393b4d9084
ms.date: 08/04/2022
ms.keywords: FindDebugInfoFileEx, FindDebugInfoFileEx function, FindDebugInfoFileExW, _win32_finddebuginfofileex, base.finddebuginfofileex, dbghelp/FindDebugInfoFileEx, dbghelp/FindDebugInfoFileExW
req.header: dbghelp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: FindDebugInfoFileExW (Unicode) and FindDebugInfoFileEx (ANSI)
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
 - FindDebugInfoFileEx
 - dbghelp/FindDebugInfoFileEx
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
 - FindDebugInfoFileEx
 - FindDebugInfoFileEx
 - FindDebugInfoFileExW
---

# FindDebugInfoFileEx function


## -description

Locates the specified 
<a href="/windows/desktop/Debug/symbol-files">debug (.dbg) file</a>.

## -parameters

### -param FileName [in]

The name of the .dbg file to locate. You can use a partial path.

### -param SymbolPath [in]

The path where symbol files are located. This can be multiple paths separated by semicolons. To retrieve the symbol path, use the 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symgetsearchpath">SymGetSearchPath</a> function.

### -param DebugFilePath [out]

A pointer to a buffer that receives the full path of the .dbg file.

### -param Callback [in, optional]

An application-defined callback function that verifies whether the correct file was found or the function should continue its search. For more information, see 
<a href="/windows/desktop/api/dbghelp/nc-dbghelp-pfind_debug_file_callback">FindDebugInfoFileProc</a>. 




This parameter may be <b>NULL</b>.

### -param CallerData [in, optional]

Optional user-defined data to pass to the callback function.

## -returns

If the function succeeds, the return value is an open handle to the .dbg file.

If the function fails, the return value is <b>NULL</b>. To retrieve extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The 
<b>FindDebugInfoFileEx</b> function is used to locate a .dbg file. This function is provided so the search can be conducted in several different directories through a single function call. The <i>SymbolPath</i> parameter can contain multiple paths, with each separated by a semicolon (;). When multiple paths are specified, the function searches each specified directory for the file. When the file is located, the search stops. Thus, be sure to specify <i>SymbolPath</i> with the paths in the correct order.

If the file name specified does not include a .dbg extension, 
<b>FindDebugInfoFileEx</b> searches for the file in the following sequence:

<ol>
<li><i>SymbolPath</i>\Symbols&#92;<i>ext</i>&#92;<i>filename</i>.dbg</li>
<li><i>SymbolPath</i>&#92;<i>ext</i>&#92;<i>filename</i>.dbg</li>
<li><i>SymbolPath</i>&#92;<i>filename</i>.dbg</li>
<li><i>FileNamePath</i>&#92;<i>filename</i>.dbg</li>
</ol>
All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

To call the Unicode version of this function, define DBGHELP_TRANSLATE_TCHAR.

## -see-also

<a href="/windows/desktop/Debug/dbghelp-functions">DbgHelp Functions</a>



<a href="/windows/desktop/api/dbghelp/nc-dbghelp-pfind_debug_file_callback">FindDebugInfoFileProc</a>



<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symgetsearchpath">SymGetSearchPath</a>
