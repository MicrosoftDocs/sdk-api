---
UID: NF:dbghelp.SymSetScopeFromInlineContext
title: SymSetScopeFromInlineContext function
author: windows-sdk-content
description: Sets the local scope to the symbol that matches the specified address and inline context.
old-location: base\symsetscopefrominlinecontext.htm
tech.root: Debug
ms.assetid: 053163b0-2504-48fc-92c1-3839311ec657
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: SymSetScopeFromInlineContext, SymSetScopeFromInlineContext function, base.symsetscopefrominlinecontext, dbghelp/SymSetScopeFromInlineContext
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
- apiref
: 
- 
: 
- SymSetScopeFromInlineContext
: 
---

# SymSetScopeFromInlineContext function


## -description


Sets the local scope to the symbol that matches the specified address and inline 
    context.


## -parameters




### -param hProcess [in]

A handle to a process. This handle must have been previously passed to the 
      <a href="https://msdn.microsoft.com/fb1c98cb-6cd0-4218-aea4-384c24c66395">SymInitialize</a> function.


### -param Address [in]

The address.


### -param InlineContext [in]

The inline context.


## -returns



If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. To retrieve extended error 
       information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.



