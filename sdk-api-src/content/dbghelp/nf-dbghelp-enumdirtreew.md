---
UID: NF:dbghelp.EnumDirTreeW
title: EnumDirTreeW function (dbghelp.h)
description: The EnumDirTreeW (Unicode) function enumerates all occurrences of the specified file in the specified directory tree.
helpviewer_keywords: ["EnumDirTree","EnumDirTree function","EnumDirTreeW","_win32_enumdirtree","base.enumdirtree","dbghelp/EnumDirTree","dbghelp/EnumDirTreeW"]
old-location: base\enumdirtree.htm
tech.root: Debug
ms.assetid: 2dd132f3-83d4-4afd-b44d-9f8d385d6116
ms.date: 08/04/2022
ms.keywords: EnumDirTree, EnumDirTree function, EnumDirTreeW, _win32_enumdirtree, base.enumdirtree, dbghelp/EnumDirTree, dbghelp/EnumDirTreeW
req.header: dbghelp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: EnumDirTreeW (Unicode) and EnumDirTree (ANSI)
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
req.redist: DbgHelp.dll 6.0 or later
ms.custom: 19H1
f1_keywords:
 - EnumDirTreeW
 - dbghelp/EnumDirTreeW
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
 - EnumDirTree
 - EnumDirTree
 - EnumDirTreeW
---

# EnumDirTreeW function


## -description

Enumerates all occurrences of the specified file in the specified directory tree.

## -parameters

### -param hProcess [in, optional]

A handle to a process. This handle must have been previously passed to the 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-syminitialize">SymInitialize</a> function.

### -param RootPath [in]

The path where the function should begin searching for the file.

### -param InputPathName [in]

The name of the file to be found. You can specify a partial path.

### -param OutputPathBuffer [out, optional]

A pointer to a buffer that receives the full path of the file. If the function fails or does not find a matching file, this buffer will still contain the last full path that was found. 

This parameter is optional and can be <b>NULL</b>.

### -param cb [in, optional]

An application-defined callback function, or <b>NULL</b>. For more information, see 
<a href="/windows/desktop/api/dbghelp/nc-dbghelp-penumdirtree_callback">EnumDirTreeProc</a>.

### -param data [in, optional]

The user-defined data or <b>NULL</b>. This value is passed to the callback function.

## -returns

If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. To retrieve extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The search can be canceled if you register a 
<a href="/windows/desktop/api/dbghelp/nc-dbghelp-psymbol_registered_callback">SymRegisterCallbackProc64</a> callback function. For every file operation, 
<i>EnumDirTree</i> calls this callback function with CBA_DEFERRED_SYMBOL_LOAD_CANCEL. If the callback function returns <b>TRUE</b>, 
<i>EnumDirTree</i> cancels the search.

All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

To call the Unicode version of this function, define DBGHELP_TRANSLATE_TCHAR.





> [!NOTE]
> The dbghelp.h header defines EnumDirTree as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Debug/dbghelp-functions">DbgHelp Functions</a>



<a href="/windows/desktop/api/dbghelp/nc-dbghelp-penumdirtree_callback">EnumDirTreeProc</a>
