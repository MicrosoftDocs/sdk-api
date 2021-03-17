---
UID: NF:dbghelp.SymRefreshModuleList
title: SymRefreshModuleList function (dbghelp.h)
description: Refreshes the module list for the process.
helpviewer_keywords: ["SymRefreshModuleList","SymRefreshModuleList function","base.symrefreshmodulelist","dbghelp/SymRefreshModuleList"]
old-location: base\symrefreshmodulelist.htm
tech.root: Debug
ms.assetid: c1c934e5-4a0a-4cb5-bb12-d6743f034ccb
ms.date: 12/05/2018
ms.keywords: SymRefreshModuleList, SymRefreshModuleList function, base.symrefreshmodulelist, dbghelp/SymRefreshModuleList
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
req.redist: DbgHelp.dll 6.5 or later
ms.custom: 19H1
f1_keywords:
 - SymRefreshModuleList
 - dbghelp/SymRefreshModuleList
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
 - SymRefreshModuleList
---

# SymRefreshModuleList function


## -description

Refreshes the module list for the process.

## -parameters

### -param hProcess [in]

A handle to a process. This handle must have been previously passed to the 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-syminitialize">SymInitialize</a> function.

## -returns

If the function succeeds, the return value is <b>TRUE</b>.
						

If the function fails, the return value is <b>FALSE</b>. To retrieve extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

This function enumerates the loaded modules for the process and effectively calls the 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symloadmodule">SymLoadModule64</a> function for each module. This same process is performed by <a href="/windows/desktop/api/dbghelp/nf-dbghelp-syminitialize">SymInitialize</a> if <i>fInvadeProcess</i> is <b>TRUE</b>.

All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

## -see-also

<a href="/windows/desktop/Debug/dbghelp-functions">DbgHelp Functions</a>