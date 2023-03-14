---
UID: NF:wow64apiset.Wow64SetThreadContext
title: Wow64SetThreadContext
ms.date: 11/18/2022
targetos: Windows
description: Sets the thread context.
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
 - Wow64SetThreadContext
f1_keywords:
 - Wow64SetThreadContext
 - wow64apiset/Wow64SetThreadContext
dev_langs:
 - c++
helpviewer_keywords:
 - Wow64SetThreadContext
---

## -description

Sets the thread context.

## -parameters

### -param hThread

A handle to the thread.

### -param lpContext

The thread context.

## -returns

Returns **True** if the context is set. Otherwise, **False**.

## -remarks

## -see-also
