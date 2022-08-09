---
UID: NF:dbghelp.SearchTreeForFile
title: SearchTreeForFile function (dbghelp.h)
description: The SearchTreeForFile function (dbghelp.h) searches a directory tree for a specified file.
helpviewer_keywords: ["SearchTreeForFile","SearchTreeForFile function","SearchTreeForFileW","_win32_searchtreeforfile","base.searchtreeforfile","dbghelp/SearchTreeForFile","dbghelp/SearchTreeForFileW"]
old-location: base\searchtreeforfile.htm
tech.root: Debug
ms.assetid: dc641de0-8e22-402e-be64-f3231ba9ed8c
ms.date: 08/04/2022
ms.keywords: SearchTreeForFile, SearchTreeForFile function, SearchTreeForFileW, _win32_searchtreeforfile, base.searchtreeforfile, dbghelp/SearchTreeForFile, dbghelp/SearchTreeForFileW
req.header: dbghelp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SearchTreeForFileW (Unicode) and SearchTreeForFile (ANSI)
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
 - SearchTreeForFile
 - dbghelp/SearchTreeForFile
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
 - SearchTreeForFile
 - SearchTreeForFile
 - SearchTreeForFileW
---

# SearchTreeForFile function


## -description

Searches a directory tree for a specified file.

## -parameters

### -param RootPath [in]

The path where the function should begin searching for the file.

### -param InputPathName [in]

The file for which the function will search. You can use a partial path.

### -param OutputPathBuffer [out]

A pointer to a buffer that receives the full path to the file that is found. This string is not modified if the return value is <b>FALSE</b>.

## -returns

If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. To retrieve extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The function searches for the file specified by the <i>InputPathName</i> parameter beginning at the path specified in the <i>RootPath</i> parameter. The maximum path depth that is allowed in the <i>RootPath</i> is 32 directories. When the function finds the file in the directory tree, it places the full path to the file in the buffer specified by the <i>OutputPathBuffer</i> parameter. The underlying file system specifies the order of the subdirectory search.

The search can be canceled if you register a 
<a href="/windows/desktop/api/dbghelp/nc-dbghelp-psymbol_registered_callback">SymRegisterCallbackProc64</a> callback function. For every directory searched, 
<b>SearchTreeForFile</b> calls this callback function with CBA_DEFERRED_SYMBOL_LOAD_CANCEL. If the callback function returns <b>TRUE</b>, 
<b>SearchTreeForFile</b> cancels the search.

This function triggers one CBA_DEFERRED_SYMBOL_LOAD_CANCEL event per directory searched. This allows the caller to cancel the search.

All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

To call the Unicode version of this function, define DBGHELP_TRANSLATE_TCHAR.

## -see-also

<a href="/windows/desktop/Debug/dbghelp-functions">DbgHelp Functions</a>
