---
UID: NF:evntrace.OpenTraceFromRealTimeLoggerWithAllocationOptions
tech.root: ETW
title: OpenTraceFromRealTimeLoggerWithAllocationOptions
ms.date: 07/12/2024
targetos: Windows
description: Creates a trace processing session attached to an active real-time ETW session.
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
 - OpenTraceFromRealTimeLoggerWithAllocationOptions
f1_keywords:
 - OpenTraceFromRealTimeLoggerWithAllocationOptions
 - evntrace/OpenTraceFromRealTimeLoggerWithAllocationOptions
dev_langs:
 - c++
helpviewer_keywords:
 - OpenTraceFromRealTimeLoggerWithAllocationOptions
---

# OpenTraceFromRealTimeLoggerWithAllocationOptions function

## -description

Creates a trace processing session attached to an active real-time ETW session.

## -parameters

### -param LoggerName

Name of the real-time event tracing session, or **NULL** if processing data from a log file. Specify a value for this member if you are calling **OpenTraceFromRealTimeLoggerWithAllocationOptions** to consume data from a real-time session.

When calling **OpenTraceFromRealTimeLoggerWithAllocationOptions**, if _LogFileHeader_ is non-**NULL** then _LoggerName_ must be **NULL**.

You can only consume events in real time if the trace controller has set the **LogFileMode** member of [EVENT_TRACE_PROPERTIES](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) to include the **EVENT_TRACE_REAL_TIME_MODE** flag.

Only users with administrative privileges, users in the Performance Log Users group, and applications running as LocalSystem, LocalService, NetworkService can consume events in real time. To grant a restricted user the ability to consume events in real time, add them to the Performance Log Users group or call [EventAccessControl](/windows/desktop/api/evntcons/nf-evntcons-eventaccesscontrol).

### -param Options

Configuration options for this processing session. See [ETW_OPEN_TRACE_OPTIONS](ns-evntrace-etw_open_trace_options.md) for more details.

### -param AllocationSize

The size, in bytes, of the memory that will be pre-allocated to store ETW buffers during processing. A larger allocation will reduce the need for individual allocation/free calls at the cost of higher consistent memory usage. This will be adjusted upward to a minimum of the total buffer space of the underlying Real-Time ETW session to ensure enough is allocated for basic functioning. If 0, the default size will be used.

### -param MemoryPartitionHandle

The handle to the Memory Partition that should be used for memory allocations for this processing session. If NULL, the Memory Partition of the process will be used. See [MemExtendedParameterPartitionHandle](../winnt/ne-winnt-mem_extended_parameter_type.md) for more details.

### -param LogFileHeader

Header information for the log file. See [TRACE_LOGFILE_HEADER](ns-evntrace-trace_logfile_header.md) for more details.

## -returns

A TRACEHANDLE that is used to identify this processing session. Typically passed to [ProcessTrace](nf-evntrace-processtrace.md) to begin processing and to [CloseTrace](nf-evntrace-closetrace.md) to end processing.

## -remarks

Once [ProcessTrace](nf-evntrace-processtrace.md) is called on the returned **TRACEHANDLE**, this will receive buffers from the ETW session as they are flushed and immediately begin processing them and calling the callbacks specified in the Options. This is identical to OpenTraceFromRealTime except that it allows customization of memory allocations for the processing session.

## -see-also
