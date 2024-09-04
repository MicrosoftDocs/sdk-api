---
UID: NF:evntrace.OpenTraceFromBufferStream
tech.root: ETW
title: OpenTraceFromBufferStream
ms.date: 07/12/2024
targetos: Windows
description: Creates a trace processing session that is not directly attached to any file or active session.
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
 - OpenTraceFromBufferStream
f1_keywords:
 - OpenTraceFromBufferStream
 - evntrace/OpenTraceFromBufferStream
dev_langs:
 - c++
helpviewer_keywords:
 - OpenTraceFromBufferStream
---

# OpenTraceFromBufferStream function

## -description

Creates a trace processing session that is not directly attached to any file or active session.

## -parameters

### -param Options

Configuration options for this processing session. See [ETW_OPEN_TRACE_OPTIONS](ns-evntrace-etw_open_trace_options.md) for more details

### -param BufferCompletionCallback

When the processing session is done with a buffer passed in from [ProcessTraceAddBufferToBufferStream](nf-evntrace-processtraceaddbuffertobufferstream.md), it will invoke this callback to allow for any freeing or other cleanup that may be required for that buffer.

### -param BufferCompletionContext

User-provided context that will be passed to the [BufferCompletionCallback](nc-evntrace-petw_buffer_completion_callback.md).

## -returns

A TRACEHANDLE that is used to identify this processing session. Typically passed to [ProcessTrace](nf-evntrace-processtrace.md) to begin processing and to [CloseTrace](nf-evntrace-closetrace.md) to end processing.

## -remarks

The caller is expected to supply the data for the trace by calling [ProcessTraceAddBufferToBufferStream](nf-evntrace-processtraceaddbuffertobufferstream.md). This is typically used for remote real-time trace processing: a remote system uses [OpenTraceFromRealTimeLogger](nf-evntrace-opentracefromrealtimelogger.md) and [ProcessTrace](nf-evntrace-processtrace.md) with a [BufferCallback](nc-evntrace-petw_buffer_callback.md) that sends buffers over the network to a local system, then the local system calls [OpenTraceFromBufferStream](nf-evntrace-opentracefrombufferstream.md) and [ProcessTrace](nf-evntrace-processtrace.md), receives buffers from the network and feeds them to the local trace processor using [ProcessTraceAddBufferToBufferStream](nf-evntrace-processtraceaddbuffertobufferstream.md).

This processing mode requires that the buffers be provided in the same order that the buffers were received from [ProcessTrace](nf-evntrace-processtrace.md) (for example, the first buffer contains header information and subsequent buffers are ordered by flush time). The only supported means to generate buffers in this way is from the [BufferCallback](nc-evntrace-petw_buffer_callback.md) from another [OpenTraceFromBufferStream](nf-evntrace-opentracefrombufferstream.md), [OpenTraceFromFile](nf-evntrace-opentracefromfile.md), [OpenTraceFromRealTimeLogger](nf-evntrace-opentracefromrealtimelogger.md), [OpenTraceFromRealTimeLoggerWithAllocationOptions](nf-evntrace-opentracefromrealtimeloggerwithallocationoptions.md) processing session.

## -see-also

