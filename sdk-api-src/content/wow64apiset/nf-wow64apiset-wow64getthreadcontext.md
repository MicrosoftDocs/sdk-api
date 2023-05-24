---
UID: NF:wow64apiset.Wow64GetThreadContext
title: Wow64GetThreadContext
ms.date: 11/17/2022
targetos: Windows
description: Retrieves the thread context.
tech.root: fs
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: Kernel32.dll
req.header: wow64apiset.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: Kernel32.lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10 version 1903
req.target-min-winversvr: Windows Server, version 1903
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - DllExport
api_location:
 - wow64apiset.h
api_name:
 - Wow64GetThreadContext
f1_keywords:
 - Wow64GetThreadContext
 - wow64apiset/Wow64GetThreadContext
dev_langs:
 - c++
helpviewer_keywords:
 - Wow64GetThreadContext
---

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
