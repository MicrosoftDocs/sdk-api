---
UID: NF:dbghelp.SymSetContext
title: SymSetContext function (dbghelp.h)
description: Sets context information used by the SymEnumSymbols function. This function only works with PDB symbols.
helpviewer_keywords: ["SymSetContext","SymSetContext function","_win32_symsetcontext","base.symsetcontext","dbghelp/SymSetContext"]
old-location: base\symsetcontext.htm
tech.root: Debug
ms.assetid: 0a9c6bfe-5e60-48c4-af98-b910df3032d5
ms.date: 12/05/2018
ms.keywords: SymSetContext, SymSetContext function, _win32_symsetcontext, base.symsetcontext, dbghelp/SymSetContext
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
req.redist: DbgHelp.dll 5.1 or later
ms.custom: 19H1
f1_keywords:
 - SymSetContext
 - dbghelp/SymSetContext
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
 - SymSetContext
---

# SymSetContext function


## -description

Sets context information used by the 
    <a href="/windows/desktop/api/dbghelp/nf-dbghelp-symenumsymbols">SymEnumSymbols</a> function. This function only works with 
    PDB symbols.

## -parameters

### -param hProcess [in]

A handle to a process. This handle must have been previously passed to the 
      <a href="/windows/desktop/api/dbghelp/nf-dbghelp-syminitialize">SymInitialize</a> function.

### -param StackFrame [in]

A pointer to an <a href="/windows/desktop/api/dbghelp/ns-dbghelp-imagehlp_stack_frame">IMAGEHLP_STACK_FRAME</a> 
      structure that contains frame information.

### -param Context [in, optional]

This parameter is ignored.

## -returns

If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. To retrieve extended error 
       information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

If you call <b>SymSetContext</b> to set the context to its 
    current value, the function fails but <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> 
    returns <b>ERROR_SUCCESS</b>.

All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to 
    this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize 
    all concurrent calls from more than one thread to this function.

## -see-also

<a href="/windows/desktop/Debug/dbghelp-functions">DbgHelp Functions</a>



<a href="/windows/desktop/api/dbghelp/ns-dbghelp-imagehlp_stack_frame">IMAGEHLP_STACK_FRAME</a>



<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symenumsymbols">SymEnumSymbols</a>