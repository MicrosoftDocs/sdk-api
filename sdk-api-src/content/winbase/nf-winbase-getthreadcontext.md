---
UID: NF:winbase.GetThreadContext
title: GetThreadContext function (winbase.h)
description: Retrieves the context of the specified thread.
helpviewer_keywords: ["GetThreadContext","GetThreadContext function","base.getthreadcontext","winbase/GetThreadContext"]
old-location: base\getthreadcontext.htm
tech.root: Debug
ms.assetid: 1bac28e1-3558-43c4-97e4-d8bb9514c38e
ms.date: 06/12/2025
ms.keywords: GetThreadContext, GetThreadContext function, base.getthreadcontext, winbase/GetThreadContext
f1_keywords:
- winbase/GetThreadContext
dev_langs:
- c++
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Kernel32.dll
api_name:
- GetThreadContext
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GetThreadContext function

## -description

Retrieves the thread context.

## -parameters

### -param hThread

A handle to the thread.

### -param lpContext

The thread context.

## -returns

Returns **True** if the context is retrieved. Otherwise, **False**.

## -remarks

## -see-also


