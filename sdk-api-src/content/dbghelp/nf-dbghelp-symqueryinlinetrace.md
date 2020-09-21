---
UID: NF:dbghelp.SymQueryInlineTrace
title: SymQueryInlineTrace function (dbghelp.h)
description: Queries an inline trace.
helpviewer_keywords: ["SymQueryInlineTrace","SymQueryInlineTrace function","base.symqueryinlinetrace","dbghelp/SymQueryInlineTrace"]
old-location: base\symqueryinlinetrace.htm
tech.root: Debug
ms.assetid: e65cf979-f482-4019-ab67-5e908d23bcfa
ms.date: 12/05/2018
ms.keywords: SymQueryInlineTrace, SymQueryInlineTrace function, base.symqueryinlinetrace, dbghelp/SymQueryInlineTrace
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
req.lib: DbgHelp.lib
req.dll: DbgHelp.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: DbgHelp.dll 6.2 or later
ms.custom: 19H1
f1_keywords:
 - SymQueryInlineTrace
 - dbghelp/SymQueryInlineTrace
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
 - SymQueryInlineTrace
---

# SymQueryInlineTrace function


## -description

Queries an inline trace.

## -parameters

### -param hProcess [in]

A handle to a process. This handle must have been previously passed to the 
      <a href="/windows/desktop/api/dbghelp/nf-dbghelp-syminitialize">SymInitialize</a> function.

### -param StartAddress [in]

The start address.

### -param StartContext [in]

Contains the context of the start of block.

### -param StartRetAddress [in]

Contains the return address of the start of the current block/

### -param CurAddress [in]

Contains the current address.

### -param CurContext [out]

Address of a <b>DWORD</b> that receives the current context.

### -param CurFrameIndex [out]

If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. To retrieve extended error 
       information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

Either the <i>StartAddress</i> or <i>StartRetAddress</i> parameters must be within the same function scope as the <i>CurAddress</i> parameter. The former indicates a step-over within the same function and the latter indicates a step-over from <i>StartAddress</i>.