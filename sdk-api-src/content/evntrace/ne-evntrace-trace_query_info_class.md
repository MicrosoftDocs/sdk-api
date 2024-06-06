---
UID: NE:evntrace._TRACE_QUERY_INFO_CLASS
title: TRACE_QUERY_INFO_CLASS (evntrace.h)
description:
  Used with EnumerateTraceGuidsEx and TraceSetInformation to specify a type of
  trace information.
helpviewer_keywords:
  [
    "MaxTraceSetInfoClass",
    "TRACE_INFO_CLASS",
    "TRACE_INFO_CLASS enumeration [ETW]",
    "TRACE_INFO_CLASS",
    "TRACE_QUERY_INFO_CLASS",
    "TRACE_INFO_CLASS",
    "TRACE_QUERY_INFO_CLASS enumeration [ETW]",
    "TRACE_QUERY_INFO_CLASS",
    "TraceDisallowListQuery",
    "TraceGroupQueryInfo",
    "TraceGroupQueryList",
    "TraceGuidQueryInfo",
    "TraceGuidQueryList",
    "TraceGuidQueryProcess",
    "TraceMaxLoggersQuery",
    "TracePeriodicCaptureStateInfo",
    "TracePeriodicCaptureStateListInfo",
    "TracePmcCounterListInfo",
    "TracePmcEventListInfo",
    "TraceProfileSourceConfigInfo",
    "TraceProfileSourceListInfo",
    "TraceProviderBinaryTracking",
    "TraceSampledProfileIntervalInfo",
    "TraceSetDisallowList",
    "TraceStackTracingInfo",
    "TraceSystemTraceEnableFlagsInfo",
    "TraceVersionInfo",
    "etw.trace_info_class",
    "evntrace/MaxTraceSetInfoClass",
    "evntrace/TRACE_INFO_CLASS",
    "evntrace/TraceDisallowListQuery",
    "evntrace/TraceGroupQueryInfo",
    "evntrace/TraceGroupQueryList",
    "evntrace/TraceGuidQueryInfo",
    "evntrace/TraceGuidQueryList",
    "evntrace/TraceGuidQueryProcess",
    "evntrace/TraceMaxLoggersQuery",
    "evntrace/TracePeriodicCaptureStateInfo",
    "evntrace/TracePeriodicCaptureStateListInfo",
    "evntrace/TracePmcCounterListInfo",
    "evntrace/TracePmcEventListInfo",
    "evntrace/TraceProfileSourceConfigInfo",
    "evntrace/TraceProfileSourceListInfo",
    "evntrace/TraceProviderBinaryTracking",
    "evntrace/TraceSampledProfileIntervalInfo",
    "evntrace/TraceSetDisallowList",
    "evntrace/TraceStackTracingInfo",
    "evntrace/TraceSystemTraceEnableFlagsInfo",
    "evntrace/TraceVersionInfo",
  ]
old-location: etw\trace_info_class.htm
tech.root: ETW
ms.assetid: b163e120-454a-48ba-93a9-71351fc3f2c2
ms.date: 12/05/2018
ms.keywords:
  MaxTraceSetInfoClass, TRACE_INFO_CLASS, TRACE_INFO_CLASS enumeration [ETW],
  TRACE_INFO_CLASS,TRACE_QUERY_INFO_CLASS,
  TRACE_INFO_CLASS,TRACE_QUERY_INFO_CLASS enumeration [ETW],
  TRACE_QUERY_INFO_CLASS, TraceDisallowListQuery, TraceGroupQueryInfo,
  TraceGroupQueryList, TraceGuidQueryInfo, TraceGuidQueryList,
  TraceGuidQueryProcess, TraceMaxLoggersQuery, TracePeriodicCaptureStateInfo,
  TracePeriodicCaptureStateListInfo, TracePmcCounterListInfo,
  TracePmcEventListInfo, TraceProfileSourceConfigInfo,
  TraceProfileSourceListInfo, TraceProviderBinaryTracking,
  TraceSampledProfileIntervalInfo, TraceSetDisallowList, TraceStackTracingInfo,
  TraceSystemTraceEnableFlagsInfo, TraceVersionInfo, etw.trace_info_class,
  evntrace/MaxTraceSetInfoClass, evntrace/TRACE_INFO_CLASS,
  evntrace/TraceDisallowListQuery, evntrace/TraceGroupQueryInfo,
  evntrace/TraceGroupQueryList, evntrace/TraceGuidQueryInfo,
  evntrace/TraceGuidQueryList, evntrace/TraceGuidQueryProcess,
  evntrace/TraceMaxLoggersQuery, evntrace/TracePeriodicCaptureStateInfo,
  evntrace/TracePeriodicCaptureStateListInfo, evntrace/TracePmcCounterListInfo,
  evntrace/TracePmcEventListInfo, evntrace/TraceProfileSourceConfigInfo,
  evntrace/TraceProfileSourceListInfo, evntrace/TraceProviderBinaryTracking,
  evntrace/TraceSampledProfileIntervalInfo, evntrace/TraceSetDisallowList,
  evntrace/TraceStackTracingInfo, evntrace/TraceSystemTraceEnableFlagsInfo,
  evntrace/TraceVersionInfo
req.header: evntrace.h
req.include-header:
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver:
req.umdf-ver:
req.ddi-compliance:
req.unicode-ansi:
req.idl:
req.max-support:
req.namespace:
req.assembly:
req.type-library:
req.lib:
req.dll:
req.irql:
targetos: Windows
req.typenames: TRACE_QUERY_INFO_CLASS, TRACE_INFO_CLASS
req.redist:
ms.custom: 19H1
f1_keywords:
  - _TRACE_QUERY_INFO_CLASS
  - evntrace/_TRACE_QUERY_INFO_CLASS
  - TRACE_QUERY_INFO_CLASS
  - evntrace/TRACE_QUERY_INFO_CLASS
dev_langs:
  - c++
topic_type:
  - APIRef
  - kbSyntax
api_type:
  - HeaderDef
api_location:
  - Evntrace.h
api_name:
  - TRACE_INFO_CLASS, TRACE_QUERY_INFO_CLASS
---

# TRACE_QUERY_INFO_CLASS enumeration

## -description

Used with [EnumerateTraceGuidsEx](/windows/desktop/ETW/enumeratetraceguidsex),
[TraceQueryInformation](/windows/desktop/ETW/tracequeryinformation), or
[TraceSetInformation](/windows/desktop/ETW/tracesetinformation) to specify a
type of trace information.

Note that **TRACE_INFO_CLASS** and **TRACE_QUERY_INFO_CLASS** are typedefs for
the same enumeration.

More comprehensive documentation about which APIs the values in the enumeration
should be used with, as well as the corresponding buffer input and output
formats are available in-line in the `TRACE_QUERY_INFO_CLASS` enumeration
definition in `evntrace.h`.

## -enum-fields

### -field TraceGuidQueryList:0

Query for an array of GUIDs of the providers that are registered on the
computer.

### -field TraceGuidQueryInfo:1

Query for information that each session used to enable the provider.

### -field TraceGuidQueryProcess:2

Query for an array of GUIDs of the providers that registered themselves in the
same process as the calling process.

### -field TraceStackTracingInfo:3

Query the setting for call stack tracing for kernel events.

Returns an array of [CLASSIC_EVENT_ID](/windows/desktop/ETW/classic-event-id)
structures. The structures specify the event GUIDs for which stack tracing is
enabled. The array is limited to 256 elements.

The value is supported on Windows 7, Windows Server 2008 R2, and later.

### -field TraceSystemTraceEnableFlagsInfo:4

Query the setting for the **EnableFlags** for the system trace provider. For
more information, see the
[EVENT_TRACE_PROPERTIES](/windows/desktop/ETW/event-trace-properties) structure.

The value is supported on Windows 8, Windows Server 2012, and later.

### -field TraceSampledProfileIntervalInfo:5

Queries the setting for the sampling profile interval for the supplied source.

The value is supported on Windows 8, Windows Server 2012, and later.

### -field TraceProfileSourceConfigInfo:6

Configures the list of profiling sources that will be collected when the
performance monitoring counter profile event fires. The collected counters will
be emitted as part of the `PERF_PMC_PROFILE` event.

The value is supported on Windows 8, Windows Server 2012, and later.

### -field TraceProfileSourceListInfo:7

Queries the list of profiling sources available on the system.

The value is supported on Windows 8, Windows Server 2012, and later.

### -field TracePmcEventListInfo:8

Configures the session with a list of system events for which performance
monitoring counters configured by `TracePmcCounterListInfo` will be collected.

The value is supported on Windows 8, Windows Server 2012, and later.

### -field TracePmcCounterListInfo:9

Configures the session with a list of profiling sources that will be collected
when events configured by `TracePmcEventListInfo` are logged to the session.

The value is supported on Windows 8, Windows Server 2012, and later.

### -field TraceSetDisallowList:10

Set the list of providers that will not be enabled to this session as part of a
provider group enablement. For more information, see
[Provider Traits](/windows/desktop/ETW/provider-traits).

The value is supported on Windows 10, Windows Server 2016, and later.

### -field TraceVersionInfo:11

Query the trace file version information.

The value is supported on Windows 10, Windows Server 2016, and later.

### -field TraceGroupQueryList:12

Query an array of GUIDs of the provider groups that are active on the computer.

### -field TraceGroupQueryInfo:13

The value is supported on Windows 10, Windows Server 2016, and later.

Query information that each session used to enable the provider group.

### -field TraceDisallowListQuery:14

The value is supported on Windows 10, Windows Server 2016, and later.

Query an array of GUIDs that are disallowed for group enables on this session.

The value is supported on Windows 10, Windows Server 2016, and later.

### -field TraceInfoReserved15

Reserved for future use. Do not use.

### -field TracePeriodicCaptureStateListInfo:16

Updates the session with a list of providers that will periodically receive the
`EVENT_CONTROL_CODE_CAPTURE_STATE` control code, akin to a call from
[EnableTraceEx2](/windows/desktop/ETW/enabletraceex2).

For more information, see
[TRACE_PERIODIC_CAPTURE_STATE_INFO](/windows/win32/api/evntrace/ns-evntrace-trace_periodic_capture_state_info).

The value is supported on Windows 10, version 1709, Windows Server, version
1709, and later.

### -field TracePeriodicCaptureStateInfo:17

Queries the limits of periodic capture state settings on the system, including
the minimum time frequency and maximum number of providers that can be
simultaneously configured.

For more information, see
[TRACE_PERIODIC_CAPTURE_STATE_INFO](/windows/win32/api/evntrace/ns-evntrace-trace_periodic_capture_state_info).

The value is supported on Windows 10, version 1709, Windows Server, version
1709, and later.

### -field TraceProviderBinaryTracking:18

Instructs ETW to begin tracking binaries for all providers that are enabled to
the session. The tracking applies to providers that are enabled to the session
at the time of the call as well as to all future providers that are enabled to
the session.

ETW generates tracking events that contain a mapping between provider GUID(s)
and the path to the module containing the callback for the tracked provider. In
the case of a realtime session, the events are provided live in the realtime
buffers. In the case of a file-based session (i.e. if the trace is saved to an
.etl file), the events are aggregated and written to the file header; they will
be among the first events the ETW runtime provides when the .etl file is played
back.

The binary tracking events will have provider id `EventTraceGuid` and opcode
`0x43`.

The value is supported on Windows 10, version 1709, Windows Server, version
1709, and later.

### -field TraceMaxLoggersQuery:19

Queries the currently configured maximum number of ETW logging sessions allowed
by the operating system. Returns a ULONG. Used with
[EnumerateTraceGuidsEx](/windows/desktop/ETW/enumeratetraceguidsex).

The value is supported on Windows 10, version 1709, Windows Server, version
1709, and later.

### -field TraceLbrConfigurationInfo:20

Enables Last Branch Record tracing for the given session, and configures
corresponding LBR filters.

The value is supported on Windows 10, version 19H1, Windows Server, version
1903, and later.

### -field TraceLbrEventListInfo:21

Configures the list of events that will trigger ETW to trace Last Branch Record
information as configured by `TraceLbrConfigurationInfo`.

The value is supported on Windows 10, version 19H1, Windows Server, version
1903, and later.

### -field TraceMaxPmcCounterQuery:22

Queries the maximum number of profiling sources that may be simultaneously
configured for use with ETW.

The value is supported on Windows 10, version 19H1, Windows Server, version
1903, and later.

### -field TraceStreamCount:23

Queries the configured stream count for a session. This is usually, but not
always, equal to the number of processors on the system, or 1 if no
per-processor buffering is configured for the session.

The value is supported on Windows 10, version 21H2, Windows Server 2022, and
later.

### -field TraceStackCachingInfo:24

Instructs ETW to begin caching stack traces for RegisterTraceGuids-based
("Classic") events in this session.

The value is supported on Windows 10, version 21H2, Windows Server 2022, and
later.

### -field TracePmcCounterOwners:25

Queries ETW for a list of processor performance monitoring counters currently in
use. This list may contain counters in use by facilities other than ETW.

The value is supported on Windows 10, version 21H2, Windows Server 2022, and
later.

### -field TraceUnifiedStackCachingInfo:26

Instructs ETW to begin caching stack traces for both RegisterTraceGuids-based
("Classic") and EventRegister-based events.

The value is supported on Windows 10, version 21H2, Windows Server 2022, and
later.

### -field TracePmcSessionInformation:27

Query all sessions for their PMC configuration set via `TracePmcEventListInfo` and `TracePmcCounterListInfo`.

The value is supported on Windows 10, version 22H2 and later.

### -field TraceContextRegisterInfo:28

Configures the session with a list of system events for which context register
events will be collected. Context register events contain CPU register
contents at the moment the specified related event is fired.

The value is supported on Windows Server 23H2 and later.

### -field MaxTraceSetInfoClass:29

Marks the last value in the enumeration. Do not use.

## -remarks

The **TRACE_INFO_CLASS** and **TRACE_QUERY_INFO_CLASS** enumerations both define
the same values. Use both enumerations with the
[EnumerateTraceGuidsEx](/windows/desktop/ETW/enumeratetraceguidsex) function or
the [TraceSetInformation](/windows/desktop/ETW/tracesetinformation) function.

## -see-also

[EnumerateTraceGuidsEx](/windows/desktop/ETW/enumeratetraceguidsex)

[TraceSetInformation](/windows/desktop/ETW/tracesetinformation)
