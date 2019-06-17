---
UID: NF:dbghelp.SymSetScopeFromInlineContext
title: SymSetScopeFromInlineContext function (dbghelp.h)
author: windows-sdk-content
description: Sets the local scope to the symbol that matches the specified address and inline context.
old-location: base\symsetscopefrominlinecontext.htm
tech.root: Debug
ms.assetid: 053163b0-2504-48fc-92c1-3839311ec657
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: SymSetScopeFromInlineContext, SymSetScopeFromInlineContext function, base.symsetscopefrominlinecontext, dbghelp/SymSetScopeFromInlineContext
ms.topic: function
f1_keywords: ["dbghelp/SymSetScopeFromInlineContext"]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - DbgHelp.dll
api_name:
 - SymSetScopeFromInlineContext
product: Windows
targetos: Windows
req.typenames: 
req.redist: DbgHelp.dll 6.2 or later
ms.custom: 19H1
---

# SymSetScopeFromInlineContext function


## -description


Sets the local scope to the symbol that matches the specified address and inline 
    context.


## -parameters




### -param hProcess [in]

A handle to a process. This handle must have been previously passed to the 
      <a href="https://docs.microsoft.com/windows/desktop/api/dbghelp/nf-dbghelp-syminitialize">SymInitialize</a> function.


### -param Address [in]

The address.


### -param InlineContext [in]

The inline context.


## -returns



If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. To retrieve extended error 
       information, call <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.



