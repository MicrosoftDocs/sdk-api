---
UID: NF:dbghelp.SymSrvStoreSupplementW
title: SymSrvStoreSupplementW function (dbghelp.h)
description: The SymSrvStoreSupplementW (Unicode) function (dbghelp.h) stores a file in the specified supplement to a symbol store.
helpviewer_keywords: ["SymSrvStoreSupplement","SymSrvStoreSupplement function","SymSrvStoreSupplementW","base.symsrvstoresupplement","dbghelp/SymSrvStoreSupplement","dbghelp/SymSrvStoreSupplementW"]
old-location: base\symsrvstoresupplement.htm
tech.root: Debug
ms.assetid: 579bd9ff-cb23-426b-8188-6897d83ada28
ms.date: 08/04/2022
ms.keywords: SymSrvStoreSupplement, SymSrvStoreSupplement function, SymSrvStoreSupplementW, base.symsrvstoresupplement, dbghelp/SymSrvStoreSupplement, dbghelp/SymSrvStoreSupplementW
req.header: dbghelp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SymSrvStoreSupplementW (Unicode) and SymSrvStoreSupplement (ANSI)
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
 - SymSrvStoreSupplementW
 - dbghelp/SymSrvStoreSupplementW
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
 - SymSrvStoreSupplement
 - SymSrvStoreSupplement
 - SymSrvStoreSupplementW
---

## -description

Stores a file in the specified supplement to a symbol store. The file is typically associated with a file in the symbol server.

## -parameters

### -param hProcess [in]

A handle to a process. This handle must have been previously passed to the 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-syminitialize">SymInitialize</a> function.

### -param SymPath [in, optional]

The path to the symbol store.

### -param Node [in]

The symbol file associated with the supplemental file.

### -param File [in]

The name of the file.

### -param Flags [in]

If this parameter is <b>SYMSTOREOPT_COMPRESS</b>, the file is compressed in the symbol store. Currently, there are no other supported values.

## -returns

If the function succeeds, the return value is the fully qualified path for the supplemental file.
						

If the function fails, the return value is <b>NULL</b>. To retrieve extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

An important use for this function is to store delta files. For more information, see <a href="/windows/desktop/api/dbghelp/nf-dbghelp-symsrvdeltaname">SymSrvDeltaName</a>.

This function returns a pointer to a buffer that may be reused by another function. Therefore, be sure to copy the data returned to another buffer immediately.

The symbol server stores supplemental files with the same extension in a common directory. For example, Sup1.xml would be stored in the following directory: <i>SymPath</i>\supplement&#92;<i>Node</i>\xml.

The administrator of a store can prevent users from writing supplemental files by creating a read-only file in the root of the store named Supplement. Alternatively, the administrator can create the supplement directory and use ACLs to control access.

All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

To call the Unicode version of this function, define DBGHELP_TRANSLATE_TCHAR.





> [!NOTE]
> The dbghelp.h header defines SymSrvStoreSupplement as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Debug/dbghelp-functions">DbgHelp Functions</a>



<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symsrvgetsupplement">SymSrvGetSupplement</a>
