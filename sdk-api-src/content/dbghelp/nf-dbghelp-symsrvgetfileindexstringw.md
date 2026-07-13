---
UID: NF:dbghelp.SymSrvGetFileIndexStringW
title: SymSrvGetFileIndexStringW function (dbghelp.h)
description: The SymSrvGetFileIndexStringW (Unicode) function (dbghelp.h) retrieves the index string for the specified .pdb, .dbg, or image file.
helpviewer_keywords: ["SymSrvGetFileIndexString","SymSrvGetFileIndexString function","SymSrvGetFileIndexStringW","base.symsrvgetfileindexstring","dbghelp/SymSrvGetFileIndexString","dbghelp/SymSrvGetFileIndexStringW"]
old-location: base\symsrvgetfileindexstring.htm
tech.root: Debug
ms.assetid: e66598fb-d7c7-4fde-a995-bfd1e7ceb24b
ms.date: 08/04/2022
ms.keywords: SymSrvGetFileIndexString, SymSrvGetFileIndexString function, SymSrvGetFileIndexStringW, base.symsrvgetfileindexstring, dbghelp/SymSrvGetFileIndexString, dbghelp/SymSrvGetFileIndexStringW
req.header: dbghelp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SymSrvGetFileIndexStringW (Unicode) and SymSrvGetFileIndexString (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: DbgHelp.lib
req.dll: DbgHelp.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: DbgHelp.dll 6.3 or later
ms.custom: 19H1
f1_keywords:
 - SymSrvGetFileIndexStringW
 - dbghelp/SymSrvGetFileIndexStringW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - DbgHelp.dll
api_name:
 - SymSrvGetFileIndexString
 - SymSrvGetFileIndexString
 - SymSrvGetFileIndexStringW
---

# SymSrvGetFileIndexStringW function


## -description

Retrieves the index string for the specified .pdb, .dbg, or image file.

## -parameters

### -param hProcess [in]

A handle to a process. This handle must have been previously passed to the 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-syminitialize">SymInitialize</a> function.

### -param SrvPath [in, optional]

The path to the symbol server.

### -param File [in]

The name of the file.

### -param Index [out]

A pointer to a 
buffer that receives the index string.

### -param Size [in]

The size of 
the <i>Index</i> buffer, in characters.

### -param Flags [in]

This parameter is reserved for future use.

## -returns

If the function succeeds, the return value is <b>TRUE</b>.
						

If the function fails, the return value is <b>FALSE</b>. To retrieve extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

This function is not for general use.  Those writing utilities for the management of files in symbol server stores may use to this function to predict the relative path the symbol server will look for a file.  It is used by srctool.exe to actually populate symbol server stores.

All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

To call the Unicode version of this function, define DBGHELP_TRANSLATE_TCHAR.





> [!NOTE]
> The dbghelp.h header defines SymSrvGetFileIndexString as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Debug/dbghelp-functions">DbgHelp Functions</a>
