---
UID: NE:evntrace._TRACE_QUERY_INFO_CLASS
title: TRACE_QUERY_INFO_CLASS (evntrace.h)
description: Determines the type of information to include with the trace.
helpviewer_keywords: ["MaxTraceSetInfoClass","TRACE_INFO_CLASS","TRACE_INFO_CLASS enumeration [ETW]","TRACE_INFO_CLASS","TRACE_QUERY_INFO_CLASS","TRACE_INFO_CLASS","TRACE_QUERY_INFO_CLASS enumeration [ETW]","TRACE_QUERY_INFO_CLASS","TraceDisallowListQuery","TraceGroupQueryInfo","TraceGroupQueryList","TraceGuidQueryInfo","TraceGuidQueryList","TraceGuidQueryProcess","TraceMaxLoggersQuery","TracePeriodicCaptureStateInfo","TracePeriodicCaptureStateListInfo","TracePmcCounterListInfo","TracePmcEventListInfo","TraceProfileSourceConfigInfo","TraceProfileSourceListInfo","TraceProviderBinaryTracking","TraceSampledProfileIntervalInfo","TraceSetDisallowList","TraceStackTracingInfo","TraceSystemTraceEnableFlagsInfo","TraceVersionInfo","etw.trace_info_class","evntrace/MaxTraceSetInfoClass","evntrace/TRACE_INFO_CLASS","evntrace/TraceDisallowListQuery","evntrace/TraceGroupQueryInfo","evntrace/TraceGroupQueryList","evntrace/TraceGuidQueryInfo","evntrace/TraceGuidQueryList","evntrace/TraceGuidQueryProcess","evntrace/TraceMaxLoggersQuery","evntrace/TracePeriodicCaptureStateInfo","evntrace/TracePeriodicCaptureStateListInfo","evntrace/TracePmcCounterListInfo","evntrace/TracePmcEventListInfo","evntrace/TraceProfileSourceConfigInfo","evntrace/TraceProfileSourceListInfo","evntrace/TraceProviderBinaryTracking","evntrace/TraceSampledProfileIntervalInfo","evntrace/TraceSetDisallowList","evntrace/TraceStackTracingInfo","evntrace/TraceSystemTraceEnableFlagsInfo","evntrace/TraceVersionInfo"]
old-location: etw\trace_info_class.htm
tech.root: ETW
ms.assetid: b163e120-454a-48ba-93a9-71351fc3f2c2
ms.date: 12/05/2018
ms.keywords: MaxTraceSetInfoClass, TRACE_INFO_CLASS, TRACE_INFO_CLASS enumeration [ETW], TRACE_INFO_CLASS,TRACE_QUERY_INFO_CLASS, TRACE_INFO_CLASS,TRACE_QUERY_INFO_CLASS enumeration [ETW], TRACE_QUERY_INFO_CLASS, TraceDisallowListQuery, TraceGroupQueryInfo, TraceGroupQueryList, TraceGuidQueryInfo, TraceGuidQueryList, TraceGuidQueryProcess, TraceMaxLoggersQuery, TracePeriodicCaptureStateInfo, TracePeriodicCaptureStateListInfo, TracePmcCounterListInfo, TracePmcEventListInfo, TraceProfileSourceConfigInfo, TraceProfileSourceListInfo, TraceProviderBinaryTracking, TraceSampledProfileIntervalInfo, TraceSetDisallowList, TraceStackTracingInfo, TraceSystemTraceEnableFlagsInfo, TraceVersionInfo, etw.trace_info_class, evntrace/MaxTraceSetInfoClass, evntrace/TRACE_INFO_CLASS, evntrace/TraceDisallowListQuery, evntrace/TraceGroupQueryInfo, evntrace/TraceGroupQueryList, evntrace/TraceGuidQueryInfo, evntrace/TraceGuidQueryList, evntrace/TraceGuidQueryProcess, evntrace/TraceMaxLoggersQuery, evntrace/TracePeriodicCaptureStateInfo, evntrace/TracePeriodicCaptureStateListInfo, evntrace/TracePmcCounterListInfo, evntrace/TracePmcEventListInfo, evntrace/TraceProfileSourceConfigInfo, evntrace/TraceProfileSourceListInfo, evntrace/TraceProviderBinaryTracking, evntrace/TraceSampledProfileIntervalInfo, evntrace/TraceSetDisallowList, evntrace/TraceStackTracingInfo, evntrace/TraceSystemTraceEnableFlagsInfo, evntrace/TraceVersionInfo
f1_keywords:
- evntrace/TRACE_INFO_CLASS, TRACE_QUERY_INFO_CLASS
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Evntrace.h
api_name:
- TRACE_INFO_CLASS, TRACE_QUERY_INFO_CLASS
targetos: Windows
req.typenames: TRACE_QUERY_INFO_CLASS, TRACE_INFO_CLASS
req.redist: 
ms.custom: 19H1
---

# TRACE_QUERY_INFO_CLASS enumeration


## -description


Determines the type of information to include with the trace.


## -enum-fields




### -field TraceGuidQueryList

Query an array of GUIDs of the providers that are registered on the computer.


### -field TraceGuidQueryInfo

Query information that each session used to enable the provider.


### -field TraceGuidQueryProcess

Query an array of GUIDs of the providers that registered themselves in the same process as the calling process.


### -field TraceStackTracingInfo

Query the setting for call stack tracing for kernel events. 

The value is supported on Windows 7, Windows Server 2008 R2, and later. 


### -field TraceSystemTraceEnableFlagsInfo

Query the setting for the <b>EnableFlags</b> for the system trace provider. For more information, see the <a href="https://docs.microsoft.com/windows/desktop/ETW/event-trace-properties">EVENT_TRACE_PROPERTIES</a> structure. 

The value is supported on Windows 8, Windows Server 2012, and later. 


### -field TraceSampledProfileIntervalInfo

Queries the setting for the sampling profile interval for the supplied source. 

The value is supported on Windows 8, Windows Server 2012, and later. 


### -field TraceProfileSourceConfigInfo

Query which sources will be traced. 

The value is supported on Windows 8, Windows Server 2012, and later. 


### -field TraceProfileSourceListInfo

Query the setting for sampled profile list information. 

The value is supported on Windows 8, Windows Server 2012, and later. 


### -field TracePmcEventListInfo

Query the list of system events on which performance monitoring counters will be collected.

The value is supported on Windows 8, Windows Server 2012, and later. 


### -field TracePmcCounterListInfo

Query the list of performance monitoring counters to  collect 

The value is supported on Windows 8, Windows Server 2012, and later. 


### -field TraceSetDisallowList

Set the list of providers that are disabled for a provider group enable on this session. For more information, see <a href="https://docs.microsoft.com/windows/desktop/ETW/provider-traits">Provider Traits</a>


The value is supported on Windows 10. 


### -field TraceVersionInfo

Query the trace file version information.

The value is supported on Windows 10.


### -field TraceGroupQueryList

Query an array of GUIDs of the provider groups that are active on the computer.


### -field TraceGroupQueryInfo

Query information that each session used to enable the provider group.


### -field TraceDisallowListQuery

Query an array of GUIDs that are disallowed for group enables on this session.


### -field TraceCompressionInfo


### -field TracePeriodicCaptureStateListInfo

Query the list of periodic capture states to collect. 


### -field TracePeriodicCaptureStateInfo

Queries the settings used for periodic capture state.


### -field TraceProviderBinaryTracking

Instructs ETW to begin tracking binaries for all providers that are enabled to the session. The tracking applies retroactively for providers that were enabled to the session prior to the call, as well as for all future providers that are enabled to the session. 

 ETW fabricates tracking events for these tracked providers that contain a mapping between provider GUID(s). ETW also fabricates the file path that describes where the registered provider is located on disk. If the session is in realtime, the events are provided live in the realtime buffers. If the session is file-based (i.e. trace is saved to an .etl file), the events are aggregated and written to the file header; they will be among some of the first events the ETW runtime provides when the .etl file is played back.

 



The binary tracking events will come from the EventTraceGuid provider, with an opcode of <b>WMI_LOG_TYPE_BINARY_PATH</b>.

The value is supported on Windows 10, version 1709 and later.


### -field TraceMaxLoggersQuery

Queries the currently-configured maximum number of system loggers allowed by the operating system.  Returns a ULONG.  Used with <a href="https://docs.microsoft.com/windows/desktop/ETW/enumeratetraceguidsex">EnumerateTraceGuidsEx</a>.

The value is supported on Windows 10, version 1709 and later.


### -field MaxTraceSetInfoClass

Marks the last value in the enumeration. Do not use.


## -remarks



The <b>TRACE_INFO_CLASS</b> and <b>TRACE_QUERY_INFO_CLASS</b> enumerations both define the same values. Use both enumerations with the <a href="https://docs.microsoft.com/windows/desktop/ETW/enumeratetraceguidsex">EnumerateTraceGuidsEx</a> function or the <a href="https://docs.microsoft.com/windows/desktop/ETW/tracesetinformation">TraceSetInformation</a> function. 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/ETW/enumeratetraceguidsex">EnumerateTraceGuidsEx</a>



<a href="https://docs.microsoft.com/windows/desktop/ETW/tracesetinformation">TraceSetInformation</a>
 

 

