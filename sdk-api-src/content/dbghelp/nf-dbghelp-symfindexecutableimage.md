---
UID: NF:dbghelp.SymFindExecutableImage
title: SymFindExecutableImage function (dbghelp.h)
description: The SymFindExecutableImage function (dbghelp.h) locates an executable file in the process search path.
helpviewer_keywords: ["SymFindExecutableImage","SymFindExecutableImage function","SymFindExecutableImageW","base.symfindexecutableimage","dbghelp/SymFindExecutableImage","dbghelp/SymFindExecutableImageW"]
old-location: base\symfindexecutableimage.htm
tech.root: Debug
ms.assetid: e81ff4bd-b9a0-4c90-86cb-67e721e2fd1b
ms.date: 08/04/2022
ms.keywords: SymFindExecutableImage, SymFindExecutableImage function, SymFindExecutableImageW, base.symfindexecutableimage, dbghelp/SymFindExecutableImage, dbghelp/SymFindExecutableImageW
req.header: dbghelp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SymFindExecutableImageW (Unicode) and SymFindExecutableImage (ANSI)
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
 - SymFindExecutableImage
 - dbghelp/SymFindExecutableImage
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
 - SymFindExecutableImage
 - SymFindExecutableImage
 - SymFindExecutableImageW
---

# SymFindExecutableImage function


## -description

Locates an executable file in the process search path.

## -parameters

### -param hProcess [in]

A handle to the process that was originally passed to the 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-syminitialize">SymInitialize</a> function.

### -param FileName [in]

The name of the executable file. You can use a partial path.

### -param ImageFilePath [out]

The fully qualified path of the executable file. This buffer must be at least MAX_PATH characters.

### -param Callback [in]

An application-defined callback function that verifies whether the correct executable file was found, or whether the function should continue its search. For more information, see 
<a href="/windows/desktop/api/dbghelp/nc-dbghelp-pfind_exe_file_callback">FindExecutableImageProc</a>. 




This parameter can be <b>NULL</b>.

### -param CallerData [in]

A user-defined value or <b>NULL</b>. This value is simply passed to the callback function. This parameter is typically used by an application to pass a pointer to a data structure that provides some context for the callback function.

## -returns

If the function succeeds, the return value is an open handle to the executable file.

If the function fails, the return value is <b>NULL</b>. To retrieve extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

This function uses the search path set using the 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-syminitialize">SymInitialize</a> or <a href="/windows/desktop/api/dbghelp/nf-dbghelp-symsetsearchpath">SymSetSearchPath</a> function.

All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

To call the Unicode version of this function, define DBGHELP_TRANSLATE_TCHAR.

## -see-also

<a href="/windows/desktop/Debug/dbghelp-functions">DbgHelp Functions</a>



<a href="/windows/desktop/api/dbghelp/nc-dbghelp-pfind_exe_file_callback">FindExecutableImageProc</a>
