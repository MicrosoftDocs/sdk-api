---
UID: NF:dbghelp.FindExecutableImageEx
title: FindExecutableImageEx function (dbghelp.h)
description: The FindExecutableImageEx function (dbghelp.h) locates the specified executable file.
helpviewer_keywords: ["FindExecutableImageEx","FindExecutableImageEx function","FindExecutableImageExW","_win32_findexecutableimageex","base.findexecutableimageex","dbghelp/FindExecutableImageEx","dbghelp/FindExecutableImageExW"]
old-location: base\findexecutableimageex.htm
tech.root: Debug
ms.assetid: 7571e168-2e91-4c97-9139-8225d28cc399
ms.date: 08/04/2022
ms.keywords: FindExecutableImageEx, FindExecutableImageEx function, FindExecutableImageExW, _win32_findexecutableimageex, base.findexecutableimageex, dbghelp/FindExecutableImageEx, dbghelp/FindExecutableImageExW
req.header: dbghelp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: FindExecutableImageExW (Unicode) and FindExecutableImageEx (ANSI)
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
 - FindExecutableImageEx
 - dbghelp/FindExecutableImageEx
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
 - FindExecutableImageEx
 - FindExecutableImageEx
 - FindExecutableImageExW
---

# FindExecutableImageEx function


## -description

Locates the specified executable file.

## -parameters

### -param FileName [in]

The name of the symbol file to be located. This parameter can be a partial path.

### -param SymbolPath [in]

The path where symbol files are located. This string can contain multiple paths separated by semicolons. To retrieve the symbol path, use the 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symgetsearchpath">SymGetSearchPath</a> function.

### -param ImageFilePath [out]

A pointer to a buffer that receives the full path of the executable file.

### -param Callback [in, optional]

An application-defined callback function that verifies whether the correct executable file was found, or whether the function should continue its search. For more information, see 
<a href="/windows/desktop/api/dbghelp/nc-dbghelp-pfind_exe_file_callback">FindExecutableImageProc</a>. 




This parameter can be <b>NULL</b>.

### -param CallerData [in, optional]

Optional user-defined data for the callback function. This parameter can be <b>NULL</b>.

## -returns

If the function succeeds, the return value is an open handle to the executable file.

If the function fails, the return value is <b>NULL</b>. To retrieve extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The 
<b>FindExecutableImageEx</b> function is provided so executable files can be found in several different directories by using a single function call. If the <i>SymbolPath</i> parameter contains multiple paths, the function searches each specified directory tree for the executable file. When the file is found, the search stops. Thus, be sure to specify <i>SymbolPath</i> with the paths in the correct order.

All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

To call the Unicode version of this function, define DBGHELP_TRANSLATE_TCHAR.

## -see-also

<a href="/windows/desktop/Debug/dbghelp-functions">DbgHelp Functions</a>



<a href="/windows/desktop/api/dbghelp/nc-dbghelp-pfind_exe_file_callback">FindExecutableImageProc</a>



<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symgetsearchpath">SymGetSearchPath</a>
