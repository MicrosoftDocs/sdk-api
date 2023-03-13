---
UID: NF:evntrace.ProcessTraceBufferDecrementReference
tech.root: ETW
title: ProcessTraceBufferDecrementReference
ms.date: 11/21/2022
targetos: Windows
description: Releases a reference to a Buffer that was added by ProcessTraceBufferIncrementReference.
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll:
  Sechost.dll on Windows 8.1 and Windows Server 2012 R2; Advapi32.dll on
  Windows 8, Windows Server 2012, Windows 7, Windows Server 2008 R2, Windows
  Server 2008, Windows Vista and Windows XP
req.header: evntrace.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib:
  Sechost.lib on Windows 8.1 and Windows Server 2012 R2; Advapi32.lib on
  Windows 8, Windows Server 2012, Windows 7, Windows Server 2008 R2, Windows
  Server 2008, Windows Vista and Windows XP
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.target-type: Windows
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
  - DllExport
api_location:
 - evntrace.h
api_name:
 - ProcessTraceBufferDecrementReference
f1_keywords:
 - ProcessTraceBufferDecrementReference
 - evntrace/ProcessTraceBufferDecrementReference
dev_langs:
 - c++
helpviewer_keywords:
 - ProcessTraceBufferDecrementReference
---

# ProcessTraceBufferDecrementReference function

## -description

Releases a reference to a Buffer that was added by [ProcessTraceBufferIncrementReference](nf-evntrace-processtracebufferincrementreference.md).

## -parameters

### -param Buffer

The buffer to decrement a reference from.

## -returns

Win32 Error Code.

## -remarks

## -see-also
