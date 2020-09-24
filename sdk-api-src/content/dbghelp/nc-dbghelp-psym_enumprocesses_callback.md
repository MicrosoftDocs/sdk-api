---
UID: NC:dbghelp.PSYM_ENUMPROCESSES_CALLBACK
title: PSYM_ENUMPROCESSES_CALLBACK (dbghelp.h)
description: An application-defined function used with the SymEnumProcesses function.
helpviewer_keywords: ["PSYM_ENUMPROCESSES_CALLBACK","SymEnumProcessesProc","SymEnumProcessesProc callback","SymEnumProcessesProc callback function","base.symenumprocessesproc","dbghelp/SymEnumProcessesProc"]
old-location: base\symenumprocessesproc.htm
tech.root: Debug
ms.assetid: 4748b2a3-0b7b-4d9c-96ed-c4b3ba927107
ms.date: 12/05/2018
ms.keywords: PSYM_ENUMPROCESSES_CALLBACK, SymEnumProcessesProc, SymEnumProcessesProc callback, SymEnumProcessesProc callback function, base.symenumprocessesproc, dbghelp/SymEnumProcessesProc
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: DbgHelp.dll 6.3 or later
ms.custom: 19H1
f1_keywords:
 - PSYM_ENUMPROCESSES_CALLBACK
 - dbghelp/PSYM_ENUMPROCESSES_CALLBACK
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - DbgHelp.h
api_name:
 - SymEnumProcessesProc
---

# PSYM_ENUMPROCESSES_CALLBACK callback function


## -description

An application-defined function used with the <a href="/windows/desktop/api/dbghelp/nf-dbghelp-symenumprocesses">SymEnumProcesses</a> function.

The <b>PSYM_ENUMPROCESSES_CALLBACK</b> type defines a pointer to this callback function. 
<b>SymEnumProcessesProc</b> is a placeholder for the application-defined function name.

## -parameters

### -param hProcess [in]

A handle to the process.

### -param UserContext [in]

The user-defined value passed from the 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symenumprocesses">SymEnumProcesses</a> function, or <b>NULL</b>. This parameter is typically used by an application to pass a pointer to a data structure that provides context information for the callback function.

## -returns

If the function returns <b>TRUE</b>, the enumeration will continue.
						

If the function returns <b>FALSE</b>, the enumeration will stop.

## -see-also

<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symenumprocesses">SymEnumProcesses</a>