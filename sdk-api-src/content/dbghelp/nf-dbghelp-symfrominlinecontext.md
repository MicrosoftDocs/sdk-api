---
UID: NF:dbghelp.SymFromInlineContext
title: SymFromInlineContext function (dbghelp.h)
description: Retrieves symbol information for the specified address and inline context.
helpviewer_keywords: ["SymFromInlineContext","SymFromInlineContext function","SymFromInlineContextW","base.symfrominlinecontext","dbghelp/SymFromInlineContext","dbghelp/SymFromInlineContextW"]
old-location: base\symfrominlinecontext.htm
tech.root: Debug
ms.assetid: a60a345e-d723-4275-bc2d-01e13ea57d67
ms.date: 12/05/2018
ms.keywords: SymFromInlineContext, SymFromInlineContext function, SymFromInlineContextW, base.symfrominlinecontext, dbghelp/SymFromInlineContext, dbghelp/SymFromInlineContextW
f1_keywords:
- dbghelp/SymFromInlineContext
dev_langs:
- c++
req.header: dbghelp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SymFromInlineContextW (Unicode) and SymFromInlineContext (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: DbgHelp.lib
req.dll: DbgHelp.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- DbgHelp.dll
api_name:
- SymFromInlineContext
- SymFromInlineContext
- SymFromInlineContextW
targetos: Windows
req.typenames: 
req.redist: DbgHelp.dll 6.2 or later
ms.custom: 19H1
---

# SymFromInlineContext function


## -description


Retrieves symbol information for the specified address and inline context.


## -parameters




### -param hProcess [in]

A handle to a process. This handle must have been previously passed to the 
      <a href="https://docs.microsoft.com/windows/desktop/api/dbghelp/nf-dbghelp-syminitialize">SymInitialize</a> function.


### -param Address [in]

The address for which a symbol should be located. The address does not have to be on a symbol boundary. If 
      the address comes after the beginning of a symbol and before the end of the symbol, the symbol is found.


### -param InlineContext [in]

The inline context for which a symbol should be located.


### -param Displacement [out, optional]

The displacement from the beginning of the symbol, or zero.


### -param Symbol [in, out]

A pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/dbghelp/ns-dbghelp-symbol_info">SYMBOL_INFO</a> structure that 
      provides information about the symbol. The symbol name is variable in length; therefore this buffer must be 
      large enough to hold the name stored at the end of the 
      <b>SYMBOL_INFO</b> structure. Be sure to set the 
      <b>MaxNameLen</b> member to the number of bytes reserved for the name.


## -returns



If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. To retrieve extended error 
       information, call <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.



