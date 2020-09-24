---
UID: NF:dbghelp.SymEnumSourceFileTokens
title: SymEnumSourceFileTokens function (dbghelp.h)
description: Enumerates all individual entries in a module's source server data, if available.
helpviewer_keywords: ["SymEnumSourceFileTokens","SymEnumSourceFileTokens function","base.symenumsourcefiletokens","dbghelp/SymEnumSourceFileTokens"]
old-location: base\symenumsourcefiletokens.htm
tech.root: Debug
ms.assetid: 0377ef07-bf9f-4938-8fc4-ae14373db590
ms.date: 12/05/2018
ms.keywords: SymEnumSourceFileTokens, SymEnumSourceFileTokens function, base.symenumsourcefiletokens, dbghelp/SymEnumSourceFileTokens
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
req.redist: DbgHelp.dll 6.8 or later
ms.custom: 19H1
f1_keywords:
 - SymEnumSourceFileTokens
 - dbghelp/SymEnumSourceFileTokens
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
 - SymEnumSourceFileTokens
---

# SymEnumSourceFileTokens function


## -description

Enumerates all individual entries in a module's <a href="/windows/desktop/Debug/source-server-and-source-indexing">source server</a> data, if available.

## -parameters

### -param hProcess [in]

A handle to a process. This handle must have been previously passed to the 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-syminitialize">SymInitialize</a> function.

### -param Base [in]

The base address of the module.

### -param Callback [in]

A 
<a href="/windows/desktop/api/dbghelp/nc-dbghelp-penumsourcefiletokenscallback">SymEnumSourceFileTokensProc</a> callback function that receives the symbol information.

## -returns

If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. To retrieve extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

Some modules have PDB files with <a href="/windows/desktop/Debug/source-server-and-source-indexing">source server</a> information detailing the version control information for each of the source files used to create each individual module.  An application can use this function to enumerate the  data for every source file that was "source indexed".

All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

## -see-also

<a href="/windows/desktop/Debug/dbghelp-functions">DbgHelp Functions</a>



<a href="/windows/desktop/Debug/source-server-and-source-indexing">Source Server</a>



<a href="/windows/desktop/api/dbghelp/nc-dbghelp-penumsourcefiletokenscallback">SymEnumSourceFileTokensProc</a>