---
UID: NS:evntrace.ETW_OPEN_TRACE_OPTIONS
tech.root: ETW
title: ETW_OPEN_TRACE_OPTIONS
ms.date: 11/21/2022
targetos: Windows
description: Provides configuration parameters to OpenTraceFromBufferStream, OpenTraceFromFile, OpenTraceFromRealTimeLogger, OpenTraceFromRealTimeLoggerWithAllocationOptions functions.
req.construct-type: structure
req.ddi-compliance: 
req.dll:
  Sechost.dll on Windows 8.1 and Windows Server 2012 R2; Advapi32.dll on
  Windows 8, Windows Server 2012, Windows 7, Windows Server 2008 R2, Windows
  Server 2008, Windows Vista and Windows XP
req.header: evntrace.h
req.include-header: 
req.kmdf-ver: 
req.lib:
  Sechost.lib on Windows 8.1 and Windows Server 2012 R2; Advapi32.lib on
  Windows 8, Windows Server 2012, Windows 7, Windows Server 2008 R2, Windows
  Server 2008, Windows Vista and Windows XP
req.max-support: 
req.redist: 
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.target-type: Windows
req.typenames: ETW_OPEN_TRACE_OPTIONS
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - evntrace.h
api_name:
 - ETW_OPEN_TRACE_OPTIONS
f1_keywords:
 - ETW_OPEN_TRACE_OPTIONS
 - evntrace/ETW_OPEN_TRACE_OPTIONS
dev_langs:
 - c++
helpviewer_keywords:
 - ETW_OPEN_TRACE_OPTIONS
---

# ETW_OPEN_TRACE_OPTIONS structure

## -description

Provides configuration parameters to [OpenTraceFromBufferStream](nf-evntrace-opentracefrombufferstream.md), [OpenTraceFromFile](nf-evntrace-opentracefromfile.md), [OpenTraceFromRealTimeLogger](nf-evntrace-opentracefromrealtimelogger.md), [OpenTraceFromRealTimeLoggerWithAllocationOptions](nf-evntrace-opentracefromrealtimeloggerwithallocationoptions.md) functions.

## -struct-fields

### -field ProcessTraceModes

A bitfield enum providing further configurations for the processing sessions. Current supported values:

- ETW_PROCESS_TRACE_MODE_NONE
- ETW_PROCESS_TRACE_MODE_RAW_TIMESTAMP – Timestamps in the EVENT_RECORD provided to the EventCallback will not be converted to file time as they are by default. Instead, they will remain in the clock type of the original event (e.g. QueryPerformanceCounter, CPU timestamp counter, or GetSystemTimeAsFileTime).

### -field EventCallback

Function pointer of type [PEVENT_RECORD_CALLBACK](nc-evntrace-pevent_record_callback.md). Called for each event in time order. If NULL then all event playback processing will be bypassed for improved performance.

### -field EventCallbackContext

User defined context that will be available in EVENT_RECORD.UserContext inside the EventCallback.

### -field BufferCallback

Called for each buffer once processing on that buffer is complete. If NULL then no buffer callback will be executed.

### -field BufferCallbackContext

User defined context that will be passed to the [BufferCallback](nc-evntrace-petw_buffer_callback.md) as the CallbackContext parameter.

## -remarks

## -see-also
