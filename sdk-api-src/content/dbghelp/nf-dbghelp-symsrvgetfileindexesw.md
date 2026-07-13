---
UID: NF:dbghelp.SymSrvGetFileIndexesW
title: SymSrvGetFileIndexesW function (dbghelp.h)
description: The SymSrvGetFileIndexesW (Unicode) function (dbghelp.h) retrieves the indexes for the specified .pdb, .dbg, or image file that would be used to store the file.
helpviewer_keywords: ["SymSrvGetFileIndexes","SymSrvGetFileIndexes function","SymSrvGetFileIndexesW","base.symsrvgetfileindexes","dbghelp/SymSrvGetFileIndexes","dbghelp/SymSrvGetFileIndexesW"]
old-location: base\symsrvgetfileindexes.htm
tech.root: Debug
ms.assetid: 9a6c6949-1ba2-4ed9-a038-68c57560454a
ms.date: 08/04/2022
ms.keywords: SymSrvGetFileIndexes, SymSrvGetFileIndexes function, SymSrvGetFileIndexesW, base.symsrvgetfileindexes, dbghelp/SymSrvGetFileIndexes, dbghelp/SymSrvGetFileIndexesW
req.header: dbghelp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SymSrvGetFileIndexesW (Unicode) and SymSrvGetFileIndexes (ANSI)
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
req.redist: DbgHelp.dll 6.3 or later
ms.custom: 19H1
f1_keywords:
 - SymSrvGetFileIndexesW
 - dbghelp/SymSrvGetFileIndexesW
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
 - SymSrvGetFileIndexes
 - SymSrvGetFileIndexes
 - SymSrvGetFileIndexesW
---

# SymSrvGetFileIndexesW function


## -description

Retrieves the indexes for the specified .pdb, .dbg, or image file that would be used to store the file. The combination of these values uniquely identifies the file in the symbol server. They can be used when calling the <a href="/windows/desktop/api/dbghelp/nf-dbghelp-symfindfileinpath">SymFindFileInPath</a> function to search for a file in a symbol store.

## -parameters

### -param File [in]

The name of the file.

### -param Id [out]

The first of three identifying parameters.

### -param Val1 [out]

The second of three identifying parameters.

### -param Val2 [out, optional]

The third of three identifying parameters.

### -param Flags [in]

This parameter is reserved for future use.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To retrieve extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

To call the Unicode version of this function, define DBGHELP_TRANSLATE_TCHAR.

## -see-also

<a href="/windows/desktop/Debug/dbghelp-functions">DbgHelp Functions</a>
