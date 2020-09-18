---
UID: NF:dbghelp.FindExecutableImage
title: FindExecutableImage function (dbghelp.h)
description: Locates an executable file.
helpviewer_keywords: ["FindExecutableImage","FindExecutableImage function","_win32_findexecutableimage","base.findexecutableimage","dbghelp/FindExecutableImage"]
old-location: base\findexecutableimage.htm
tech.root: Debug
ms.assetid: 48185a75-fa1d-4735-a814-e1f5893dd095
ms.date: 12/05/2018
ms.keywords: FindExecutableImage, FindExecutableImage function, _win32_findexecutableimage, base.findexecutableimage, dbghelp/FindExecutableImage
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
 - FindExecutableImage
 - dbghelp/FindExecutableImage
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
 - FindExecutableImage
---

# FindExecutableImage function


## -description

Locates an executable file.

To specify a callback function, use the 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-findexecutableimageex">FindExecutableImageEx</a> function.

## -parameters

### -param FileName [in]

The name of the symbol file to be located. This parameter can be a partial path.

### -param SymbolPath [in]

The path where symbol files are located. This can be multiple paths separated by semicolons. To retrieve the symbol path, use the 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symgetsearchpath">SymGetSearchPath</a> function.

### -param ImageFilePath [out]

A pointer to a buffer that receives the full path of the executable file.

## -returns

If the function succeeds, the return value is an open handle to the executable file.

If the function fails, the return value is <b>NULL</b>. To retrieve extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The 
<b>FindExecutableImage</b> function is provided so executable files can be located in several different directories through a single function call. The <i>SymbolPath</i> parameter can contain multiple paths, with each separated by a semicolon (;). When multiple paths are specified, the function searches each directory tree for the executable file. When the file is located, the search stops. Thus, be sure to specify <i>SymbolPath</i> with the paths in the correct order.

All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

## -see-also

<a href="/windows/desktop/Debug/dbghelp-functions">DbgHelp Functions</a>



<a href="/windows/desktop/api/dbghelp/nf-dbghelp-findexecutableimageex">FindExecutableImageEx</a>



<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symgetsearchpath">SymGetSearchPath</a>