---
UID: NS:evntprov._EVENT_FILTER_DESCRIPTOR
title: EVENT_FILTER_DESCRIPTOR (evntprov.h)
description:
  Defines the filter data that a session passes to the provider's enable
  callback function.
helpviewer_keywords:
  [
    "*PEVENT_FILTER_DESCRIPTOR",
    "EVENT_FILTER_DESCRIPTOR",
    "EVENT_FILTER_DESCRIPTOR structure [ETW]",
    "EVENT_FILTER_TYPE_EVENT_ID",
    "EVENT_FILTER_TYPE_EVENT_NAME",
    "EVENT_FILTER_TYPE_EXECUTABLE_NAME",
    "EVENT_FILTER_TYPE_NONE",
    "EVENT_FILTER_TYPE_PACKAGE_APP_ID",
    "EVENT_FILTER_TYPE_PACKAGE_ID",
    "EVENT_FILTER_TYPE_PAYLOAD",
    "EVENT_FILTER_TYPE_PID",
    "EVENT_FILTER_TYPE_SCHEMATIZED",
    "EVENT_FILTER_TYPE_STACKWALK",
    "EVENT_FILTER_TYPE_STACKWALK_LEVEL_KW",
    "EVENT_FILTER_TYPE_STACKWALK_NAME",
    "EVENT_FILTER_TYPE_SYSTEM_FLAGS",
    "EVENT_FILTER_TYPE_TRACEHANDLE",
    "PEVENT_FILTER_DESCRIPTOR",
    "PEVENT_FILTER_DESCRIPTOR structure pointer [ETW]",
    "_EVENT_FILTER_DESCRIPTOR",
    "base.event_filter_descriptor",
    "etw.event_filter_descriptor",
    "evntprov/EVENT_FILTER_DESCRIPTOR",
    "evntprov/PEVENT_FILTER_DESCRIPTOR",
  ]
old-location: etw\event_filter_descriptor.htm
tech.root: ETW
ms.assetid: 9318868a-29d8-4a5e-9579-c06a7c0fd78f
ms.date: 12/05/2018
ms.keywords:
  "*PEVENT_FILTER_DESCRIPTOR, EVENT_FILTER_DESCRIPTOR, EVENT_FILTER_DESCRIPTOR
  structure [ETW], EVENT_FILTER_TYPE_EVENT_ID, EVENT_FILTER_TYPE_EVENT_NAME,
  EVENT_FILTER_TYPE_EXECUTABLE_NAME, EVENT_FILTER_TYPE_NONE,
  EVENT_FILTER_TYPE_PACKAGE_APP_ID, EVENT_FILTER_TYPE_PACKAGE_ID,
  EVENT_FILTER_TYPE_PAYLOAD, EVENT_FILTER_TYPE_PID,
  EVENT_FILTER_TYPE_SCHEMATIZED, EVENT_FILTER_TYPE_STACKWALK,
  EVENT_FILTER_TYPE_STACKWALK_LEVEL_KW, EVENT_FILTER_TYPE_STACKWALK_NAME,
  EVENT_FILTER_TYPE_SYSTEM_FLAGS, EVENT_FILTER_TYPE_TRACEHANDLE,
  PEVENT_FILTER_DESCRIPTOR, PEVENT_FILTER_DESCRIPTOR structure pointer [ETW],
  _EVENT_FILTER_DESCRIPTOR, base.event_filter_descriptor,
  etw.event_filter_descriptor, evntprov/EVENT_FILTER_DESCRIPTOR,
  evntprov/PEVENT_FILTER_DESCRIPTOR"
req.header: evntprov.h
req.include-header:
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: EVENT_FILTER_DESCRIPTOR, *PEVENT_FILTER_DESCRIPTOR
req.redist:
ms.custom: 19H1
f1_keywords:
  - _EVENT_FILTER_DESCRIPTOR
  - evntprov/_EVENT_FILTER_DESCRIPTOR
  - PEVENT_FILTER_DESCRIPTOR
  - evntprov/PEVENT_FILTER_DESCRIPTOR
  - EVENT_FILTER_DESCRIPTOR
  - evntprov/EVENT_FILTER_DESCRIPTOR
dev_langs:
  - c++
topic_type:
  - APIRef
  - kbSyntax
api_type:
  - HeaderDef
api_location:
  - Evntprov.h
api_name:
  - EVENT_FILTER_DESCRIPTOR
---

# EVENT_FILTER_DESCRIPTOR structure

## -description

The **EVENT_FILTER_DESCRIPTOR** structure defines the filter data that a session
passes to the provider's enable callback function.

## -struct-fields

### -field Ptr

A pointer to the filter data for the filter type specified in the **Type**
member.

If the **Type** member is set to **EVENT_FILTER_TYPE_PID**, the **Ptr** member
points to an array of process IDs (PIDs).

If the **Type** member is set to **EVENT_FILTER_TYPE_EVENT_ID**, the **Ptr**
member points to a
[EVENT_FILTER_EVENT_ID](/windows/desktop/api/evntprov/ns-evntprov-event_filter_event_id)
structure that contains an array of event IDs and a Boolean value that
determines whether tracing is enabled or disabled for the specified event IDs.

If the **Type** member is set to **EVENT_FILTER_TYPE_STACKWALK**, the **Ptr**
member points to a
[EVENT_FILTER_EVENT_ID](/windows/desktop/api/evntprov/ns-evntprov-event_filter_event_id)
structure that contains an array of event IDs and a Boolean value that
determines whether stack tracing is enabled or disabled for the specified event
IDs.

If the **Type** member is set to **EVENT_FILTER_TYPE_SCHEMATIZED**, see the
[EVENT_FILTER_HEADER](/windows/desktop/api/evntprov/ns-evntprov-event_filter_header)
structure for details on constructing the filter.

### -field Size

The size of the data, in bytes.

The maximum data size limit varies based on the specified **Type** member (the
type of the filter). The maximum data size, in bytes, for many of the filter
types is limited to **MAX_EVENT_FILTER_DATA_SIZE**, defined in the _evntprov.h_
header file to 1024.

### -field Type

A provider-defined value that identifies the filter. For filters defined in an
instrumentation manifest, set this member to **EVENT_FILTER_TYPE_SCHEMATIZED**.

The possible values for this member are defined in the _evntprov.h_ header file.

- **EVENT_FILTER_TYPE_NONE** (0x00000000)

  No filters.

- **EVENT_FILTER_TYPE_SCHEMATIZED** (0x80000000)

  A schematized filter.

  This is the traditional filtering setup also called provider-side filtering.
  The controller defines a custom set of filters as a binary object that is
  passed to the provider in the [EnableTrace](/windows/desktop/ETW/enabletrace),
  [EnableTraceEx](/windows/desktop/ETW/enabletraceex-func), or
  [EnableTraceEx2](/windows/desktop/ETW/enabletraceex2) call. It is incumbent on
  the controller and provider to define and interpret these filters and the
  controller should only log applicable events. This requires a close coupling
  of the controller and provider since the type and format of the binary object
  of what can be filtered is not defined. The
  [TdhEnumerateProviderFilters](/windows/desktop/api/tdh/nf-tdh-tdhenumerateproviderfilters)
  function can be used to retrieve the filters defined in a manifest.

  For more information on schematized filters, see
  [Defining Filters](/windows/desktop/WES/defining-filters).

- **EVENT_FILTER_TYPE_SYSTEM_FLAGS** (0x80000001)

  Reserved for internal use.

- **EVENT_FILTER_TYPE_TRACEHANDLE** (0x80000002)

  Used to capture a rundown of a particular trace session. The _ControlCode_
  parameter passed to the
  [EnableTraceEx](/windows/desktop/ETW/enabletraceex-func) function must be set
  to **EVENT_CONTROL_CODE_CAPTURE_STATE** and the _ProviderId_ parameter must be
  the **SystemTraceControlGuid**. The **EVENT_FILTER_DESCRIPTOR** structure
  should point to a single **TRACEHANDLE** that represents a current ETW
  session. A rundown will be performed for that particular session.

- **EVENT_FILTER_TYPE_PID** (0x80000004)

  The process ID. This is one of the scope filters.

  Filtering ETW events based on process IDs will result in an event stream (file
  or real-time) that contains the events from the providers in the specified
  processes only. It will only enable the provider in the processes whose PIDs
  are provided. The list of PIDs is the PIDs of the processes running at the
  time when [EnableTraceEx2](/windows/desktop/ETW/enabletraceex2) is called and
  will enable the provider in all the processes (for which PIDs are provided) at
  that particular time. The list of PIDs will not be stored in the session. So
  when a process is terminated and then reappears, the provider in it will not
  get automatically enabled to the trace session. The PIDs based filter-blob is
  only valid for a kernel mode logger session because the private logger session
  runs inside a user-mode process.

  The maximum number of process IDs that can be filtered is limited by
  **MAX_EVENT_FILTER_PID_COUNT** defined in the _evntprov.h_ header file to 8.

  In case a process ID filter is provided, then the provider will be enabled in
  the user-mode processes only. In case, the same provider is registered by a
  kernel-mode driver, it will not be enabled.

  This is used with
  [EVENT_TRACE_PROPERTIES_V2](/windows/desktop/ETW/event-trace-properties-v2)
  for system wide private loggers.

- **EVENT_FILTER_TYPE_EXECUTABLE_NAME** (0x80000008)

  The executable file name. This is one of the scope filters.

  This is used with
  [EVENT_TRACE_PROPERTIES_V2](/windows/desktop/ETW/event-trace-properties-v2)
  for system wide private loggers.

- **EVENT_FILTER_TYPE_PACKAGE_ID** (0x80000010)

  The package ID. This is one of the scope filters

  This can be used to filter providers to events emitted from a particular
  Windows Store app package.

- **EVENT_FILTER_TYPE_PACKAGE_APP_ID** (0x80000020)

  The package relative app ID (PRAID). This is one of the scope filters

  This can be used to filter providers to events emitted from a particular
  Windows Store app package.

- **EVENT_FILTER_TYPE_PAYLOAD** (0x80000100)

  The event payload (the content of the event).

  The maximum data size, in bytes, for an event payload filter is limited to
  **MAX_EVENT_FILTER_PAYLOAD_SIZE** defined in the _evntprov.h_ header file
  to 4096.

- **EVENT_FILTER_TYPE_EVENT_ID** (0x80000200)

  The event ID.

  This feature allows enabling or disabling filtering for a list of events. The
  provided filter includes a
  [EVENT_FILTER_EVENT_ID](/windows/desktop/api/evntprov/ns-evntprov-event_filter_event_id)
  structure that contains an array of event IDs and a Boolean value that
  indicates whether to enable or disable from filtering for the specified
  events. Each event write call will go through this array quickly to find out
  whether enable or disable logging the event.

  When applied to a TraceLogging provider this filter will be ignored as
  TraceLogging events do not have static event IDs.

  The maximum number of event IDs allowed in the
  [EVENT_FILTER_EVENT_ID](/windows/desktop/api/evntprov/ns-evntprov-event_filter_event_id)
  structure is limited by **MAX_EVENT_FILTER_EVENT_ID_COUNT** defined in the
  _evntprov.h_ header file to 64.

- **EVENT_FILTER_TYPE_EVENT_NAME** (0x80000400)

  The TraceLogging event name.

  This feature allows enabling or disabling of TraceLogging events based on
  their names. The provided filter includes an
  [EVENT_FILTER_EVENT_NAME](/windows/desktop/api/evntprov/ns-evntprov-event_filter_event_name)
  structure that contains an array of event names, keyword bitmasks, and level
  to filter on, and a Boolean value that indicates whether to enable or disable
  the described events. When applied to a non-TraceLogging provider, this filter
  is ignored as those events do not have names specified in their payload.

  > **Note:** Available on Windows 10, version 1709 and later.

- **EVENT_FILTER_TYPE_STACKWALK** (0x80001000)

  A stack walk.

  When stack walking is enabled for a provider, then the stack is captured for
  all the events generated by the provider. Most of the time, the user is only
  interested in stack from only certain number of events.

  This feature allows enabling or disabling stack walking on a list of events.
  The provided filter includes a
  [EVENT_FILTER_EVENT_ID](/windows/desktop/api/evntprov/ns-evntprov-event_filter_event_id)
  structure that contains an array of event IDs and a Boolean value that
  indicates whether to enable or disable stack capturing for the specified
  events. Each event write call will go through this array quickly to find out
  whether the stack should be captured or not.

  When applied to a TraceLogging provider, this filter will be ignored as
  TraceLogging events do not have static event IDs.

  If you choose to use this filter, you still must specify
  **EVENT_ENABLE_PROPERTY_STACK_TRACE** in the
  [ENABLE_TRACE_PARAMETERS](/windows/desktop/ETW/enable-trace-parameters)
  structure when enabling the provider for any stacks to be collected from a
  provider.

  The maximum number of event IDs allowed in the
  [EVENT_FILTER_EVENT_ID](/windows/desktop/api/evntprov/ns-evntprov-event_filter_event_id)
  structure is limited by **MAX_EVENT_FILTER_EVENT_ID_COUNT** defined in the
  _evntprov.h_ header file to 64.

  > **Note:** Available on Windows 10, version 1709 and later.

- **EVENT_FILTER_TYPE_STACKWALK_NAME** (0x80002000)

  A TraceLogging event name.

  This feature allows filtering of stack collection for TraceLogging events
  based on the event names. The provided filter includes an
  [EVENT_FILTER_EVENT_NAME](/windows/desktop/api/evntprov/ns-evntprov-event_filter_event_name)
  structure that contains an array of event names, keyword bitmasks, and level
  to filter on, and a Boolean value that indicates whether to collect stacks or
  not for the described events.

  When applied to a non-TraceLogging provider, this filter is ignored as those
  events do not have names specified in their payload.

  If you choose to use this filter, you still must specify
  **EVENT_ENABLE_PROPERTY_STACK_TRACE** on the
  [ENABLE_TRACE_PARAMETERS](/windows/desktop/ETW/enable-trace-parameters)
  structure when enabling the provider for any stacks to be collected from a
  provider at all.

  > **Note:** Available on Windows 10, version 1709 and later.

- **EVENT_FILTER_TYPE_STACKWALK_LEVEL_KW** (0x80004000)

  Event level and keyword.

  This feature allows filtering of stack collection for events based on their
  level and keyword. The provided filter includes an
  [EVENT_FILTER_LEVEL_KW](/windows/desktop/api/evntprov/ns-evntprov-event_filter_level_kw)
  structure that contains keyword bitmasks and level to filter on, as well as a
  Boolean value that indicates whether to collect stacks or not for the
  described events.

  If you choose to use this filter, you still must specify
  **EVENT_ENABLE_PROPERTY_STACK_TRACE** on the
  [ENABLE_TRACE_PARAMETERS](/windows/desktop/ETW/enable-trace-parameters)
  structure when enabling the provider for any stacks to be collected from a
  provider at all.

  > **Note:** Available on Windows 10, version 1709 and later.

## -remarks

The provider determines the layout of the data and its purpose.

On Windows 8.1,Windows Server 2012 R2, and later, event payload, scope, and
stack walk filters can be used by the
[EnableTraceEx2](/windows/desktop/ETW/enabletraceex2) function and the
[ENABLE_TRACE_PARAMETERS](/windows/desktop/ETW/enable-trace-parameters) and
**EVENT_FILTER_DESCRIPTOR** structures to filter on specific conditions in a
logger session. For more information on event payload filters, see the
**EnableTraceEx2**,
[TdhCreatePayloadFilter](/windows/desktop/api/tdh/nf-tdh-tdhcreatepayloadfilter),
and
[TdhAggregatePayloadFilters](/windows/desktop/api/tdh/nf-tdh-tdhaggregatepayloadfilters)
functions and the **ENABLE_TRACE_PARAMETERS** and
[PAYLOAD_FILTER_PREDICATE](/windows/desktop/api/tdh/ns-tdh-payload_filter_predicate)
structures.

## -see-also

[Defining Filters](/windows/desktop/WES/defining-filters)

[ENABLE_TRACE_PARAMETERS](/windows/desktop/ETW/enable-trace-parameters)

[EVENT_FILTER_EVENT_ID](/windows/desktop/api/evntprov/ns-evntprov-event_filter_event_id)

[EnableCallback](/windows/desktop/api/evntprov/nc-evntprov-penablecallback)

[EnableTrace](/windows/desktop/ETW/enabletrace)

[EnableTraceEx](/windows/desktop/ETW/enabletraceex-func)

[EnableTraceEx2](/windows/desktop/ETW/enabletraceex2)

[PAYLOAD_FILTER_PREDICATE](/windows/desktop/api/tdh/ns-tdh-payload_filter_predicate)

[TdhAggregatePayloadFilters](/windows/desktop/api/tdh/nf-tdh-tdhaggregatepayloadfilters)

[TdhCreatePayloadFilter](/windows/desktop/api/tdh/nf-tdh-tdhcreatepayloadfilter)
