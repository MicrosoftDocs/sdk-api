---
UID: NF:evntrace.ProcessTraceAddBufferToBufferStream
tech.root: ETW
title: ProcessTraceAddBufferToBufferStream
ms.date: 07/15/2024
targetos: Windows
description: Provides an ETW trace buffer to a processing session created by OpenTraceFromBufferStream.
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
req.lib: Advapi32.dll
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 11 2022 Update
req.target-min-winversvr: Windows Server 2022
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
 - ProcessTraceAddBufferToBufferStream
f1_keywords:
 - ProcessTraceAddBufferToBufferStream
 - evntrace/ProcessTraceAddBufferToBufferStream
dev_langs:
 - c++
helpviewer_keywords:
 - ProcessTraceAddBufferToBufferStream
---

# ProcessTraceAddBufferToBufferStream function

## -description

Provides an ETW trace buffer to a processing session created by [OpenTraceFromBufferStream](nf-evntrace-opentracefrombufferstream.md).

## -parameters

### -param TraceHandle

The TRACEHANDLE for the processing session to add to.

### -param Buffer

A valid ETW buffer to process.

### -param BufferSize

The ETW buffer size.

## -returns

ERROR_SUCCESS or a Win32 error code to indicate that the buffer is invalid, out of time order, or that the TraceHandle is invalid.

## -remarks

Buffers passed by **ProcessTraceAddBufferToBufferStream** must be in the same order as they were produced by [ProcessTrace](nf-evntrace-processtrace.md). Incorrect ordering of buffers may cause the function to return an error.

When the buffer is done processing, the *BufferCompletionCallback* specified in [OpenTraceFromBufferStream](nf-evntrace-opentracefrombufferstream.md) will be called to release it.

## -see-also
