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
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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

Used with [EnumerateTraceGuidsEx](/windows/desktop/ETW/enumeratetraceguidsex) or
[TraceSetInformation](/windows/desktop/ETW/tracesetinformation) to specify a
type of trace information.

Note that **TRACE_INFO_CLASS** and **TRACE_QUERY_INFO_CLASS** are typedefs for
the same enumeration.

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

The value is supported on Windows 7, Windows Server 2008 R2, and later.

### -field TraceSystemTraceEnableFlagsInfo:4

Query the setting for the **EnableFlags** for the system trace provider. For
more information, see the
[EVENT_TRACE_PROPERTIES](/windows/desktop/ETW/event-trace-properties) structure.

The value is supported on Windows 8, Windows Server 2012, and later.

### -field TraceSampledProfileIntervalInfo:5

Queries the setting for the sampling profile interval for the supplied source.

The value is supported on Windows 8, Windows Server 2012, and later.

### -field TraceProfileSourceConfigInfo:6

Query which sources will be traced.

The value is supported on Windows 8, Windows Server 2012, and later.

### -field TraceProfileSourceListInfo:7

Query the setting for sampled profile list information.

The value is supported on Windows 8, Windows Server 2012, and later.

### -field TracePmcEventListInfo:8

Query the list of system events on which performance monitoring counters will be
collected.

The value is supported on Windows 8, Windows Server 2012, and later.

### -field TracePmcCounterListInfo:9

Query the list of performance monitoring counters to collect

The value is supported on Windows 8, Windows Server 2012, and later.

### -field TraceSetDisallowList:10

Set the list of providers that are disabled for a provider group enable on this
session. For more information, see
[Provider Traits](/windows/desktop/ETW/provider-traits)

The value is supported on Windows 10.

### -field TraceVersionInfo:11

Query the trace file version information.

The value is supported on Windows 10.

### -field TraceGroupQueryList:12

Query an array of GUIDs of the provider groups that are active on the computer.

### -field TraceGroupQueryInfo:13

Query information that each session used to enable the provider group.

### -field TraceDisallowListQuery:14

Query an array of GUIDs that are disallowed for group enables on this session.

### -field TraceCompressionInfo

### -field TracePeriodicCaptureStateListInfo:16

Query the list of periodic capture states to collect.

### -field TracePeriodicCaptureStateInfo:17

Queries the settings used for periodic capture state.

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

The value is supported on Windows 10, version 1709 and later.

### -field TraceMaxLoggersQuery:19

Queries the currently-configured maximum number of system loggers allowed by the
operating system. Returns a ULONG. Used with
[EnumerateTraceGuidsEx](/windows/desktop/ETW/enumeratetraceguidsex).

The value is supported on Windows 10, version 1709 and later.

### -field MaxTraceSetInfoClass

Marks the last value in the enumeration. Do not use.

## -remarks

The **TRACE_INFO_CLASS** and **TRACE_QUERY_INFO_CLASS** enumerations both define
the same values. Use both enumerations with the
[EnumerateTraceGuidsEx](/windows/desktop/ETW/enumeratetraceguidsex) function or
the [TraceSetInformation](/windows/desktop/ETW/tracesetinformation) function.

## -see-also

[EnumerateTraceGuidsEx](/windows/desktop/ETW/enumeratetraceguidsex)

[TraceSetInformation](/windows/desktop/ETW/tracesetinformation)
