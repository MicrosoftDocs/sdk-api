---
UID: NF:dbghelp.FindDebugInfoFile
title: FindDebugInfoFile function (dbghelp.h)
description: Locates a debug (.dbg) file.
helpviewer_keywords: ["FindDebugInfoFile","FindDebugInfoFile function","_win32_finddebuginfofile","base.finddebuginfofile","dbghelp/FindDebugInfoFile"]
old-location: base\finddebuginfofile.htm
tech.root: Debug
ms.assetid: a13d3bf4-f34d-4304-9d47-aa21c3fa23b8
ms.date: 12/05/2018
ms.keywords: FindDebugInfoFile, FindDebugInfoFile function, _win32_finddebuginfofile, base.finddebuginfofile, dbghelp/FindDebugInfoFile
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
 - FindDebugInfoFile
 - dbghelp/FindDebugInfoFile
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
 - FindDebugInfoFile
---

# FindDebugInfoFile function


## -description

Locates a 
<a href="/windows/desktop/Debug/symbol-files">debug (.dbg) file</a>.

To provide a callback function to verify the symbol file located, use the 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-finddebuginfofileex">FindDebugInfoFileEx</a> function.

## -parameters

### -param FileName [in]

The name of the .dbg file that is desired. You can use a partial path.

### -param SymbolPath [in]

The path where symbol files are located. This can be multiple paths separated by semicolons. To retrieve the symbol path, use the 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symgetsearchpath">SymGetSearchPath</a> function.

### -param DebugFilePath [out]

A pointer to a buffer that receives the full path of the .dbg file.

## -returns

If the function succeeds, the return value is an open handle to the .dbg file.

If the function fails, the return value is <b>NULL</b>. To retrieve extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The 
<b>FindDebugInfoFile</b> function is used to locate a .dbg file. This function is provided so the search can be conducted in several different directories through a single function call. The <i>SymbolPath</i> parameter can contain multiple paths, with each separated by a semicolon (;). When multiple paths are specified, the function searches each directory for the file. Subdirectories are not searched. When the file is located, the search stops. Thus, be sure to specify <i>SymbolPath</i> with the paths in the correct order.

All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

## -see-also

<a href="/windows/desktop/Debug/dbghelp-functions">DbgHelp Functions</a>



<a href="/windows/desktop/api/dbghelp/nf-dbghelp-finddebuginfofileex">FindDebugInfoFileEx</a>



<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symgetsearchpath">SymGetSearchPath</a>