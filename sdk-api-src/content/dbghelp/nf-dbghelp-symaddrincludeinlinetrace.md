---
UID: NF:dbghelp.SymAddrIncludeInlineTrace
title: SymAddrIncludeInlineTrace function (dbghelp.h)
description: Indicates whether the specified address is within an inline frame.
helpviewer_keywords: ["SymAddrIncludeInlineTrace","SymAddrIncludeInlineTrace function","base.symaddrincludeinlinetrace","dbghelp/SymAddrIncludeInlineTrace"]
old-location: base\symaddrincludeinlinetrace.htm
tech.root: Debug
ms.assetid: 12bb0fbf-3573-4efd-88a6-e94828906413
ms.date: 12/05/2018
ms.keywords: SymAddrIncludeInlineTrace, SymAddrIncludeInlineTrace function, base.symaddrincludeinlinetrace, dbghelp/SymAddrIncludeInlineTrace
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
 - SymAddrIncludeInlineTrace
 - dbghelp/SymAddrIncludeInlineTrace
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
 - SymAddrIncludeInlineTrace
---

# SymAddrIncludeInlineTrace function


## -description

Indicates whether the specified address is within an inline frame.

## -parameters

### -param hProcess [in]

A handle to a process. This handle must have been previously passed to the 
      <a href="/windows/desktop/api/dbghelp/nf-dbghelp-syminitialize">SymInitialize</a> function.

### -param Address [in]

The address.

## -returns

Returns zero if the address is not within an inline frame.