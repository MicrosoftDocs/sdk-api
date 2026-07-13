---
UID: NC:evntrace.PETW_BUFFER_CALLBACK
tech.root: ETW
title: PETW_BUFFER_CALLBACK
ms.date: 11/21/2022
targetos: Windows
description: Function definition for the BufferCallback that will be invoked by ProcessTrace.
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
 - LibDef
api_location:
 - evntrace.h
api_name:
 - PETW_BUFFER_CALLBACK
f1_keywords:
 - PETW_BUFFER_CALLBACK
 - evntrace/PETW_BUFFER_CALLBACK
dev_langs:
 - c++
helpviewer_keywords:
 - PETW_BUFFER_CALLBACK
---

# PETW_BUFFER_CALLBACK callback function

## -description

Function definition for the BufferCallback that will be invoked by [ProcessTrace](nf-evntrace-processtrace.md).

## -parameters

### -param Buffer

Pointer to the raw buffer data, which begins with an [ETW_BUFFER_HEADER](ns-evntrace-etw_buffer_header.md) struct and is followed by event data.

By default this buffer is available only until the callback returns. To use the buffer after the callback returns, call [ProcessTraceBufferIncrementReference](nf-evntrace-processtracebufferincrementreference.md). This will keep the buffer available until you call [ProcessTraceBufferDecrementReference](nf-evntrace-processtracebufferdecrementreference.md) on it.

ProcessTrace will not return until all such Buffer references have been decremented.

### -param BufferSize

Size of the provided *Buffer*.

### -param ConsumerInfo

Contains information on the current state of the processing session.

### -param CallbackContext

User-provided context from [ETW_OPEN_TRACE_OPTIONS.BufferCallbackContext](ns-evntrace-etw_open_trace_options.md).

## -returns

If **TRUE**, the processing will continue. If **FALSE**, trace processing will stop and [ProcessTrace](nf-evntrace-processtrace.md) will return.

## -remarks

## -see-also
