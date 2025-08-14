---
UID: NF:evntrace.EnableTraceEx2
title: EnableTraceEx2 function (evntrace.h)
description:
  A trace session controller calls EnableTraceEx2 to configure how an ETW event
  provider logs events to a trace session.
helpviewer_keywords:
  [
    "EVENT_CONTROL_CODE_CAPTURE_STATE",
    "EVENT_CONTROL_CODE_DISABLE_PROVIDER",
    "EVENT_CONTROL_CODE_ENABLE_PROVIDER",
    "EnableTraceEx2",
    "EnableTraceEx2 function [ETW]",
    "TRACE_LEVEL_CRITICAL",
    "TRACE_LEVEL_ERROR",
    "TRACE_LEVEL_INFORMATION",
    "TRACE_LEVEL_VERBOSE",
    "TRACE_LEVEL_WARNING",
    "etw.enabletraceex2",
    "evntrace/EnableTraceEx2",
  ]
old-location: etw\enabletraceex2.htm
tech.root: ETW
ms.assetid: 3aceffb6-614f-4cad-bbec-f181f0cbdbff
ms.date: 12/05/2018
ms.keywords:
  EVENT_CONTROL_CODE_CAPTURE_STATE, EVENT_CONTROL_CODE_DISABLE_PROVIDER,
  EVENT_CONTROL_CODE_ENABLE_PROVIDER, EnableTraceEx2, EnableTraceEx2 function
  [ETW], TRACE_LEVEL_CRITICAL, TRACE_LEVEL_ERROR, TRACE_LEVEL_INFORMATION,
  TRACE_LEVEL_VERBOSE, TRACE_LEVEL_WARNING, etw.enabletraceex2,
  evntrace/EnableTraceEx2
req.header: evntrace.h
req.include-header:
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
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
  Sechost.lib on Windows 8.1 and Windows Server 2012 R2; Advapi32.lib on
  Windows 8, Windows Server 2012, Windows 7 and Windows Server 2008 R2
req.dll:
  Sechost.dll on Windows 8.1 and Windows Server 2012 R2; Advapi32.dll on
  Windows 8, Windows Server 2012, Windows 7 and Windows Server 2008 R2
req.irql:
targetos: Windows
req.typenames:
req.redist:
ms.custom: 19H1
f1_keywords:
  - EnableTraceEx2
  - evntrace/EnableTraceEx2
dev_langs:
  - c++
topic_type:
  - APIRef
  - kbSyntax
api_type:
  - DllExport
api_location:
 - api-ms-win-eventing-controller-l1-1-1.dll
 - api-ms-win-downlevel-advapi32-l2-1-0.dll
 - Sechost.dll
 - Advapi32.dll
 - API-MS-Win-DownLevel-AdvAPI32-l2-1-1.dll
 - API-MS-Win-Eventing-Controller-l1-1-0.dll
 - KernelBase.dll
api_name:
  - EnableTraceEx2
---

# EnableTraceEx2 function

## -description

A trace session controller calls **EnableTraceEx2** to configure how an ETW
event provider logs events to a trace session.

This function supersedes the
[EnableTrace](/windows/win32/api/evntrace/nf-evntrace-enabletrace) and
[EnableTraceEx](/windows/win32/api/evntrace/nf-evntrace-enabletraceex)
functions.

## -parameters

### -param TraceHandle [in]

Handle of the event tracing session for which you are configuring the provider.
The [StartTrace](/windows/win32/api/evntrace/nf-evntrace-starttracea) function
returns this handle when a new trace is started. To obtain the handle of an
existing trace, use
[ControlTrace](/windows/win32/api/evntrace/nf-evntrace-controltracew) to query
the trace properties based on the trace's name and then get the handle from the
**Wnode.HistoricalContext** field of the returned `EVENT_TRACE_PROPERTIES` data.

### -param ProviderId [in]

The provider ID (control GUID) of the event provider that you want to configure.

### -param ControlCode [in]

You can specify one of the following control codes:

| Value                                   | Meaning                                                                                               |
| --------------------------------------- | ----------------------------------------------------------------------------------------------------- |
| **EVENT_CONTROL_CODE_DISABLE_PROVIDER** | Update the session configuration so that the session does not receive events from the provider.       |
| **EVENT_CONTROL_CODE_ENABLE_PROVIDER**  | Update the session configuration so that the session receives the requested events from the provider. |
| **EVENT_CONTROL_CODE_CAPTURE_STATE**    | Requests that the provider log its state information.                                                 |

### -param Level [in]

A value that indicates the maximum level of events that you want the provider to
write. The provider typically writes an event if the event's level is less than
or equal to this value, in addition to meeting the _MatchAnyKeyword_ and
_MatchAllKeyword_ criteria.

Microsoft defines the semantics of levels 1-5 as shown below. Lower values
indicate more-severe events. Each value of _Level_ enables the specified level
and all more-severe levels. For example, if you specify `TRACE_LEVEL_WARNING`,
your consumer will receive warning, error, and critical events.

| Value                           | Meaning                                    |
| ------------------------------- | ------------------------------------------ |
| **TRACE_LEVEL_CRITICAL** (1)    | Abnormal exit or termination events        |
| **TRACE_LEVEL_ERROR** (2)       | Severe error events                        |
| **TRACE_LEVEL_WARNING** (3)     | Warning events such as allocation failures |
| **TRACE_LEVEL_INFORMATION** (4) | Non-error informational events             |
| **TRACE_LEVEL_VERBOSE** (5)     | Detailed diagnostic events                 |

The `TRACE_LEVEL` constants are defined in _evntrace.h_. Equivalent
`WINMETA_LEVEL` constants are defined in _winmeta.h_.

### -param MatchAnyKeyword [in]

64-bit bitmask of keywords that determine the categories of events that you want
the provider to write. The provider typically writes an event if the event's
keyword bits match **any** of the bits set in this value or if the event has no
keyword bits set, in addition to meeting the _Level_ and _MatchAllKeyword_
criteria.

### -param MatchAllKeyword [in]

64-bit bitmask of keywords that restricts the events that you want the provider
to write. The provider typically writes an event if the event's keyword bits
match **all** of the bits set in this value or if the event has no keyword bits
set, in addition to meeting the _Level_ and _MatchAnyKeyword_ criteria.

This value is frequently set to 0.

### -param Timeout [in]

If _Timeout_ is 0, this function will start configuring the provider
asynchronously and will return immediately (i.e. it will return without waiting
for provider callbacks to complete).

Otherwise, this function will start configuring the provider and will then begin
waiting for the configuration to complete, including waiting for all provider
callbacks to complete. If configuration completes before the specified timeout,
this function will return **ERROR_SUCCESS**. Otherwise, this function will
return **ERROR_TIMEOUT**.

To wait forever, set to **INFINITE**.

### -param EnableParameters [in, optional]

The trace parameters used to enable the provider. For details, see
[ENABLE_TRACE_PARAMETERS](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters).

## -returns

If the function is successful, the return value is **ERROR_SUCCESS**.

If the function fails, the return value is one of the
[system error codes](/windows/win32/debug/system-error-codes). The following are
some common errors and their causes.

- **ERROR_INVALID_PARAMETER**

  A parameter is incorrect.

  This can occur if any of the following are true:

  - The _ProviderId_ is **NULL**.
  - The _TraceHandle_ is **0**.

- **ERROR_TIMEOUT**

  The timeout value expired before the enable callback completed. For details,
  see the _Timeout_ parameter.

- **ERROR_INVALID_FUNCTION**

  You cannot update the level when the provider is not registered.

- **ERROR_NO_SYSTEM_RESOURCES**

  Exceeded the number of trace sessions that can enable the provider.

- **ERROR_ACCESS_DENIED**

  Only users with administrative privileges, users in the
  `Performance Log Users` group, and services running as `LocalSystem`,
  `LocalService`, or `NetworkService` can enable event providers to a
  cross-process session. To grant a restricted user the ability to enable an
  event provider, add them to the `Performance Log Users` group or see
  [EventAccessControl](/windows/desktop/api/evntcons/nf-evntcons-eventaccesscontrol).

  **Windows XP and Windows 2000:** Anyone can enable an event provider.

## -remarks

Event trace controllers call this function to configure the event providers that
write events to the session. For example, a controller might call this function
to begin collecting events from a provider, to adjust the level or keywords of
the events being collected from a provider, or to stop collecting events from a
provider.

The enablement behavior for a provider depends on which APIs the provider uses.

- A provider that uses
  [RegisterTraceGuids](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa)
  (e.g. a provider using TMF-based WPP or MOF) uses the legacy enablement system
  (sometimes called "classic ETW"). When a legacy provider is enabled or
  reconfigured for a session, the ETW runtime notifies the provider and provides
  access to the level, the low 32 bits of the MatchAnyKeyword mask, and the
  session ID. The provider then uses its own logic to decide which events should
  be enabled and sends those events directly to the specified session. The event
  data sent to ETW at runtime includes the event's decode GUID and message ID
  but does not include the event's control GUID, level or keywords. ETW verifies
  that the provider has the necessary permissions and then adds the event data
  to the specified session.
  - Because the events are sent directly to a specific session with no control
    GUID, level or keyword information, ETW cannot perform any additional
    filtering or routing for providers that use the legacy enablement system.
    Each event can be routed to no more than one session.
- A provider that uses
  [EventRegister](/windows/win32/api/evntprov/nf-evntprov-eventregister) (e.g. a
  manifest-based provider or a TraceLogging provider) uses the modern enablement
  system (sometimes called "crimson ETW"). When a modern provider is enabled or
  reconfigured for a session, the ETW runtime notifies the provider with the
  level, the 64-bit MatchAnyKeyword mask, the 64-bit MatchAllKeyword mask, and
  any custom provider-side filtering data specified by the trace controller. The
  provider then uses its own logic to decide which events should be enabled,
  though most providers just duplicate the logic of
  [EventProviderEnabled](/windows/win32/api/evntprov/nf-evntprov-eventproviderenabled).
  The provider sends the enabled events to ETW for routing. The event data sent
  to ETW includes the event's control GUID, message ID, level, and keywords. ETW
  then performs additional filtering as appropriate, routing the event to the
  appropriate session(s).
  - Because the events are sent to ETW with descriptive information, ETW can
    perform additional filtering and routing before adding the event to the
    session. Events can be routed to more than one session if appropriate.

For providers that use the modern enablement system (i.e. providers using
**EventRegister**), ETW supports several features that can be requested by the
trace session controller via **EnableTraceEx2** _EnableParameters_. (See
[EVENT_FILTER_DESCRIPTOR](/windows/win32/api/evntprov/ns-evntprov-event_filter_descriptor)
for details.)

- **Schematized filtering** - This is the traditional filtering setup, also
  called provider-side filtering. The controller defines a custom set of filters
  as a binary object that is passed to the provider in
  [EnableCallback](/windows/win32/api/evntprov/nc-evntprov-penablecallback)
  _FilterData_. It is incumbent on the controller and provider to define and
  interpret these filters. The provider can then use the
  [EventWriteEx](/windows/win32/api/evntprov/nf-evntprov-eventwriteex) _Filter_
  parameter to indicate sessions to which an event should not be sent due to the
  provider-side filtering. This requires a close coupling of the controller and
  provider since the type and format of the binary object of what can be
  filtered is not defined. The
  [TdhEnumerateProviderFilters](/windows/desktop/api/tdh/nf-tdh-tdhenumerateproviderfilters)
  function can be used to retrieve the filters defined in a manifest.
- **Scope filtering** - Certain providers are enabled or not enabled to a
  session based on whether or not they meet the criteria specified by the scope
  filters. There are several types of scope filters that allow filtering based
  on the process ID (PID), executable filename, the app ID, and the app package
  name. This feature is supported on Windows 8.1, Windows Server 2012 R2, and
  later.
- **Stackwalk filtering** - This notifies ETW to only perform a stack walk for a
  given set of event IDs or (for TraceLogging events) event names. This feature
  is supported on Windows 8.1, Windows Server 2012 R2, and later.
- **Attribute filtering** - For manifest providers, events can be filtered based
  on event attributes such as level, keyword, event ID, or event name.
- **Event payload filtering** - For manifest providers, events can be filtered
  on-the-fly based on whether or not they satisfy a logical expression based on
  one or more predicates.

> [!Note]
> Even though ETW supports powerful payload and attribute filtering,
> events should primarily be filtered based scope filters or via control GUID,
> level, and keyword. Providers usually perform control GUID, level, and keyword
> filtering directly in the provider's code before the event is generated or
> sent to ETW. In most providers, events that are disabled by level or keyword
> have almost no impact on system performance. Similarly, providers disabled by
> scope filters are have almost no impact on system performance. Other kinds of
> filtering (based on payload or attributes other than level and keyword) are
> usually performed after the provider has generated the event and sent it to
> the ETW runtime, meaning the event has impact on system performance (the CPU
> time spent preparing the event and sending it to ETW) even if the ETW
> filtering determines that the event should not be recorded by any sessions.
> This kind of filtering is only effective in reducing trace data volume and is
> not as effective for reducing trace CPU overhead.

Every time **EnableTraceEx2** is called, the filters for the provider in that
session are replaced by the new parameters defined by the parameters passed to
the **EnableTraceEx2** function. Multiple filters passed in a single
**EnableTraceEx2** call can be combined with an additive effect, but filters
passed in a subsequent call will replace the previous set of filters.

To disable filtering and thereby enable all providers/events in the logging
session, call **EnableTraceEx2** with the _EnableParameters_ parameter pointing
at an
[ENABLE_TRACE_PARAMETERS](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters)
structure with the **FilterDescCount** member set to 0.

Each filter passed to the **EnableTraceEx2** function is specified by a **Type**
member in the
[EVENT_FILTER_DESCRIPTOR](/windows/desktop/api/evntprov/ns-evntprov-event_filter_descriptor).
An array of **EVENT_FILTER_DESCRIPTOR** structures is passed in the
[ENABLE_TRACE_PARAMETERS](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters)
structure passed in the **EnableParameters** parameter to the **EnableTraceEx2**
function.

Each type of filter (a specific **Type** member) may only appear once in a call
to the **EnableTraceEx2** function. Some filter types allow multiple conditions
to be included in a single filter. The maximum number of filters that can be
included in a call to **EnableTraceEx2** is set by **MAX_EVENT_FILTERS_COUNT**
(defined in the _Evntprov.h_ header file; value may change in future versions of
the Windows SDK).

Each filter type has its own size or entity limits based on the specific
**Type** member in the
[EVENT_FILTER_DESCRIPTOR](/windows/desktop/api/evntprov/ns-evntprov-event_filter_descriptor)
structure. The list below indicates these limits.

- **EVENT_FILTER_TYPE_SCHEMATIZED**

  - Filter size limit: **MAX_EVENT_FILTER_DATA_SIZE** (1024)
  - Number of elements allowed: Defined by provider and controller

- **EVENT_FILTER_TYPE_PID**

  - Filter size limit: **MAX_EVENT_FILTER_DATA_SIZE** (1024)
  - Number of elements allowed: **MAX_EVENT_FILTER_PID_COUNT** (8)

- **EVENT_FILTER_TYPE_EXECUTABLE_NAME**

  - Filter size limit: **MAX_EVENT_FILTER_DATA_SIZE** (1024)
  - Number of elements allowed: A single string that can contain multiple
    executable file names separated by semicolons.

- **EVENT_FILTER_TYPE_PACKAGE_ID**

  - Filter size limit: **MAX_EVENT_FILTER_DATA_SIZE** (1024)
  - Number of elements allowed: A single string that can contain multiple
    package IDs separated by semicolons.

- **EVENT_FILTER_TYPE_PACKAGE_APP_ID**

  - Filter size limit: **MAX_EVENT_FILTER_DATA_SIZE** (1024)
  - Number of elements allowed: A single string that can contain multiple
    package relative app IDs (PRAIDs) separated by semicolons.

- **EVENT_FILTER_TYPE_PAYLOAD**

  - Filter size limit: **MAX_EVENT_FILTER_PAYLOAD_SIZE** (4096)
  - Number of elements allowed: 1

- **EVENT_FILTER_TYPE_EVENT_ID**

  - Filter size limit: Not defined
  - Number of elements allowed: **MAX_EVENT_FILTER_EVENT_ID_COUNT** (64)

- **EVENT_FILTER_TYPE_STACKWALK**
  - Filter size limit: Not defined
  - Number of elements allowed: **MAX_EVENT_FILTER_EVENT_ID_COUNT** (64)

Keywords define event categories. For example, if the provider defines
InitializationKeyword = `0x1` (keyword bit 0), FileOperationKeyword = `0x2`
(keyword bit 1), and CalculationKeyword = `0x4` (keyword bit 2), you can set
_MatchAnyKeyword_ to (InitializationKeyword | CalculationKeyword) = 5 to receive
initialization and calculation events but not file events.

When used with modern
([manifest-based](/windows/desktop/ETW/about-event-tracing) or
[TraceLogging](/windows/desktop/tracelogging/trace-logging-about)) providers, a
_MatchAnyKeyword_ value of `0` is treated the same as a _MatchAnyKeyword_ value
of `0xFFFFFFFFFFFFFFFF`, i.e. it enables all event keywords. However, this
behavior does not apply to legacy
([MOF or TMF-based WPP](/windows/desktop/ETW/about-event-tracing)) providers. To
enable all event keywords from a legacy provider, set _MatchAnyKeyword_ to
`0xFFFFFFFF`. To enable all event keywords from both legacy and modern
providers, set _MatchAnyKeyword_ to `0xFFFFFFFFFFFFFFFF`.

If an event's keyword is zero, the provider will write the event to the session
regardless of the _MatchAnyKeyword_ and _MatchAllKeyword_ masks. (This behavior
can be disabled by using the
[EVENT_ENABLE_PROPERTY_IGNORE_KEYWORD_0](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters)
flag.)

To indicate that you wish to enable a Provider Group, use the
`EVENT_ENABLE_PROPERTY_PROVIDER_GROUP` flag on the **EnableProperty** member of
_EnableParameters_.

When you call **EnableTraceEx2**, the provider may or may not already be
registered. If the provider is already registered, ETW calls the provider's
callback function (if any), and the session begins receiving events. If the
provider is not already registered, ETW will call the provider's callback
function (if any) immediately after the provider registers and the session will
then begin receiving events. If the provider is not already registered, the
provider's callback function will not receive the source ID.

If the provider is registered and already enabled to your session, you can call
**EnableTraceEx2** again to update the _Level_, _MatchAnyKeyword_,
_MatchAllKeyword_ parameters and the **EnableProperty** and **EnableFilterDesc**
members of _EnableParameters_.

On Windows 8.1, Windows Server 2012 R2, and later, event payload, scope, and
stack walk filters can be used by the **EnableTraceEx2** function and the
[ENABLE_TRACE_PARAMETERS](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters)
and
[EVENT_FILTER_DESCRIPTOR](/windows/desktop/api/evntprov/ns-evntprov-event_filter_descriptor)
structures to filter on specific conditions in a logger session. For more
information on event payload filters, see the
[TdhCreatePayloadFilter](/windows/desktop/api/tdh/nf-tdh-tdhcreatepayloadfilter),
and
[TdhAggregatePayloadFilters](/windows/desktop/api/tdh/nf-tdh-tdhaggregatepayloadfilters)
functions and the **ENABLE_TRACE_PARAMETERS**, **EVENT_FILTER_DESCRIPTOR**, and
[PAYLOAD_FILTER_PREDICATE](/windows/desktop/api/tdh/ns-tdh-payload_filter_predicate)
structures.

Special system trace provider events cannot be enabled or disabled by
**EnableTraceEx2**. They can only be enabled via the _EnableFlags_ field of
[EVENT_TRACE_PROPERTIES](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)
when the trace is first started by
[StartTrace](/windows/win32/api/evntrace/nf-evntrace-starttracea).

Starting with Windows 11,
[system trace provider events can be enabled using EnableTraceEx2](/windows/win32/etw/system-providers).

Up to eight trace sessions can enable and receive events from the same modern
([manifest-based](/windows/desktop/ETW/about-event-tracing) or
[TraceLogging](/windows/desktop/tracelogging/trace-logging-about)) provider.
However, only one trace session can enable a legacy (MOF, TMF-based WPP)
provider. If more than one session tries to enable a legacy provider, the first
session would stop receiving events when the second session enables the same
provider. For example, if Session A enabled a legacy provider and then Session B
enabled the same provider, only Session B would receive events from that
provider.

A provider remains enabled for the session until the session disables the
provider. If the application that started the session ends without disabling the
provider, the provider remains enabled.

To determine the level and keywords used to enable a manifest-based provider,
use one of the following commands:

- logman query providers _provider-name_
- wevtutil gp _provider-name_

For classic providers, it is up to the provider to document and make available
to potential controllers the severity levels or enable flags that it supports.
If the provider wants to be enabled by any controller, the provider should
accept 0 for the severity level and enable flags and interpret 0 as a request to
perform default logging (whatever that may be).

If you use **EnableTraceEx2** to enable a classic provider, the following
translation occurs:

- The _Level_ parameter is the same as setting the _EnableLevel_ parameter in
  [EnableTrace](/windows/desktop/ETW/enabletrace).
- The _MatchAnyKeyword_ is the same as setting the _EnableFlag_ parameter in
  [EnableTrace](/windows/desktop/ETW/enabletrace) except that the keyword value
  is truncated from a 64-bit value to a 32-bit value.
- In the [ControlCallback](/windows/desktop/ETW/controlcallback) callback, the
  provider can call
  [GetTraceEnableLevel](/windows/desktop/ETW/gettraceenablelevel) to get the
  level and [GetTraceEnableFlags](/windows/desktop/ETW/gettraceenableflags) to
  get the enable flag.
- The other parameter are not used.

### Examples

The following example shows use of the **EnableTraceEx2** with payload filters
using the
[TdhCreatePayloadFilter](/windows/desktop/api/tdh/nf-tdh-tdhcreatepayloadfilter)
and
[TdhAggregatePayloadFilters](/windows/desktop/api/tdh/nf-tdh-tdhaggregatepayloadfilters)
functions to filter on specific conditions in a logger session.

```cpp
#define INITGUID
#include <windows.h>
#include <stdlib.h>
#include <stdio.h>
#include <strsafe.h>
#include <evntrace.h>
#include <tdh.h>

#define MAXIMUM_SESSION_NAME 1024

#define PATH_TO_MANIFEST_FILE L"c:\\ExampleManifest.man"

//
// The following definitions would be found in the include file generated by
// message compiler from the manifest file.
//

// Provider Example-Provider Event Count 2
EXTERN_C __declspec(selectany) const GUID EXAMPLE_PROVIDER = {0x37a59b93, 0xbb25, 0x4cee, {0x97, 0xaa, 0x8b, 0x6a, 0xcd, 0xc, 0x4d, 0xf8}};

//
// Event Descriptors
//
EXTERN_C __declspec(selectany) const EVENT_DESCRIPTOR Example_Event_1 = { 0x1, 0x0, 0x0, 0x1, 0x0, 0x0, 0x0 };
#define Example_Event_1_value 0x1
EXTERN_C __declspec(selectany) const EVENT_DESCRIPTOR Example_Event_2 = { 0x2, 0x0, 0x0, 0x1, 0x0, 0x0, 0x0 };
#define Example_Event_2_value 0x2

//
// (End of snippet from include file)
//

// Allocate an EVENT_TRACE_PROPERTIES structure and set the needed logging session properties
PEVENT_TRACE_PROPERTIES AllocateTraceProperties(
    _In_opt_ PCWSTR LoggerName,
    _In_opt_ PCWSTR LogFileName
)
{
    PEVENT_TRACE_PROPERTIES TraceProperties = NULL;
    ULONG BufferSize;

    BufferSize = sizeof(EVENT_TRACE_PROPERTIES) +
        (MAXIMUM_SESSION_NAME + MAX_PATH) * sizeof(WCHAR);

    TraceProperties = (PEVENT_TRACE_PROPERTIES)malloc(BufferSize);
    if (TraceProperties == NULL) {
        printf("Unable to allocate %d bytes for properties structure.\n", BufferSize);
        goto Exit;
    }

    //
    // Set the session properties.
    //
    ZeroMemory(TraceProperties, BufferSize);
    TraceProperties->Wnode.BufferSize = BufferSize;
    TraceProperties->Wnode.Flags = WNODE_FLAG_TRACED_GUID;
    TraceProperties->LoggerNameOffset = sizeof(EVENT_TRACE_PROPERTIES);
    TraceProperties->LogFileNameOffset = sizeof(EVENT_TRACE_PROPERTIES) +
        (MAXIMUM_SESSION_NAME * sizeof(WCHAR));

    if (LoggerName != NULL) {
        StringCchCopyW((LPWSTR)((PCHAR)TraceProperties + TraceProperties->LoggerNameOffset),
            MAXIMUM_SESSION_NAME,
            LoggerName);
    }

    if (LogFileName != NULL) {
        StringCchCopyW((LPWSTR)((PCHAR)TraceProperties + TraceProperties->LogFileNameOffset),
            MAX_PATH,
            LogFileName);
    }

Exit:
    return TraceProperties;
}

// Free the EVENT_TRACE_PROPERTIES structure previously allocated
VOID FreeTraceProperties(
    _In_ PEVENT_TRACE_PROPERTIES TraceProperties
)
{
    free(TraceProperties);
    return;
}

// Set the values needed in a PAYLOAD_FILTER_PREDICATE for a single payload filter
FORCEINLINE VOID PayloadPredicateCreate(
    _Out_ PAYLOAD_FILTER_PREDICATE* Predicate,
    _In_ PCWSTR FieldName,
    USHORT CompareOp,
    PCWSTR Value
)
{
    Predicate->FieldName = (PWSTR)FieldName;
    Predicate->CompareOp = CompareOp;
    Predicate->Value = (PWSTR)Value;
    return;
}

int __cdecl wmain()
{
    UINT i;
    PVOID EventFilters[2];
    EVENT_FILTER_DESCRIPTOR FilterDescriptor;
    UINT PredicateCount;
    PAYLOAD_FILTER_PREDICATE Predicates[3];
    ULONG FilterCount;
    ULONG Status = ERROR_SUCCESS;
    TRACEHANDLE SessionHandle = 0;
    PEVENT_TRACE_PROPERTIES TraceProperties;
    BOOLEAN TraceStarted = FALSE;
    PCWSTR LoggerName = L"MyTrace";
    ENABLE_TRACE_PARAMETERS EnableParameters;

    ZeroMemory(EventFilters, sizeof(EventFilters));
    ZeroMemory(Predicates, sizeof(Predicates));
    TraceProperties = NULL;
    FilterCount = 0;

    //
    // Load the manifest for the provider
    //
    Status = TdhLoadManifest((PWSTR)PATH_TO_MANIFEST_FILE);
    if (Status != ERROR_SUCCESS) {
        printf("TdhCreatePayloadFilter() failed with %lu\n", Status);
        goto Exit;
    }

    //
    // Create predicates that match the following high-level expression:
    //
    // INCLUDE Example_Event_1 IF
    //     Example_Event_1.Initiator == "User" AND
    //     7 <= Example_Event_1.Level <= 16
    //
    PredicateCount = 0;

    PayloadPredicateCreate(
        &Predicates[PredicateCount++],
        (PWSTR)L"Initiator",
        PAYLOADFIELD_IS,
        (PWSTR)L"User");

    PayloadPredicateCreate(
        &Predicates[PredicateCount++],
        L"Level",
        PAYLOADFIELD_BETWEEN,
        L"7,16");

    Status = TdhCreatePayloadFilter(
        &EXAMPLE_PROVIDER,
        &Example_Event_1,
        FALSE,      // Match all predicates (AND)
        PredicateCount,
        Predicates,
        &EventFilters[FilterCount++]);
    if (Status != ERROR_SUCCESS) {
        printf("TdhCreatePayloadFilter() failed with %lu\n", Status);
        goto Exit;
    }

    //
    // Create predicates that match the following high-level expression:
    // INCLUDE Example_Event_2 IF
    //      Example_Event_2.Title CONTAINS "UNI" OR
    //      Example_Event_2.InstanceId == {0E95CFBC-58D4-44BA-BE40-E63A853536DF} OR
    //      Example_Event_2.ErrorCode != 0      //
    PredicateCount = 0;

    PayloadPredicateCreate(
        &Predicates[PredicateCount++],
        L"Title",
        PAYLOADFIELD_CONTAINS,
        L"UNI");

    PayloadPredicateCreate(
        &Predicates[PredicateCount++],
        L"InstanceId",
        PAYLOADFIELD_IS,
        L" {0E95CFBC-58D4-44BA-BE40-E63A853536DF}");

    PayloadPredicateCreate(
        &Predicates[PredicateCount++],
        L"ErrorCode",
        PAYLOADFIELD_NE,
        L"0");

    Status = TdhCreatePayloadFilter(
        &EXAMPLE_PROVIDER,
        &Example_Event_2,
        FALSE,      // Match any predicates (OR)
        PredicateCount,
        Predicates,
        &EventFilters[FilterCount++]);
    if (Status != ERROR_SUCCESS) {
        printf("TdhCreatePayloadFilter() failed with %lu\n", Status);
        goto Exit;
    }

    //
    // Combine the interim filters into a final filter descriptor.
    //
    Status = TdhAggregatePayloadFilters(
        FilterCount,
        EventFilters,
        NULL,
        &FilterDescriptor);
    if (Status != ERROR_SUCCESS) {
        printf("TdhAggregatePayloadFilters() failed with %lu\n", Status);
        goto Exit;
    }

    //
    // Clean up the interim filters
    //
    for (i = 0; i < FilterCount; i++) {

        Status = TdhDeletePayloadFilter(&EventFilters[i]);
        if (Status != ERROR_SUCCESS) {
            printf("TdhDeletePayloadFilter() failed with %lu\n", Status);
            goto Exit;
        }
    }

    //
    // Create a new trace session
    //
    //
    // Allocate EVENT_TRACE_PROPERTIES structure and perform some
    // basic initialization.
    //
    // N.B. LoggerName will be populated during StartTrace call.
    //
    TraceProperties = AllocateTraceProperties(NULL, L"SystemTrace.etl");
    if (TraceProperties == NULL) {
        Status = ERROR_OUTOFMEMORY;
        goto Exit;
    }

    TraceProperties->LogFileMode = EVENT_TRACE_FILE_MODE_SEQUENTIAL | EVENT_TRACE_SYSTEM_LOGGER_MODE;
    TraceProperties->MaximumFileSize = 100; // Limit file size to 100MB max
    TraceProperties->BufferSize = 512; // Use 512KB trace buffers
    TraceProperties->MinimumBuffers = 8;
    TraceProperties->MaximumBuffers = 64;

    Status = StartTraceW(&SessionHandle, LoggerName, TraceProperties);
    if (Status != ERROR_SUCCESS) {
        printf("StartTrace() failed with %lu\n", Status);
        goto Exit;
    }

    TraceStarted = TRUE;

    //
    // Enable the provider to a trace session with filtering enabled on the
    // provider
    //
    ZeroMemory(&EnableParameters, sizeof(EnableParameters));
    EnableParameters.Version = ENABLE_TRACE_PARAMETERS_VERSION_2;
    EnableParameters.EnableFilterDesc = &FilterDescriptor;
    EnableParameters.FilterDescCount = 1;

    Status = EnableTraceEx2(
        SessionHandle,
        &EXAMPLE_PROVIDER,
        EVENT_CONTROL_CODE_ENABLE_PROVIDER,
        TRACE_LEVEL_VERBOSE,
        0,
        0,
        0,
        &EnableParameters);
    if (Status != ERROR_SUCCESS) {
        printf("EnableTraceEx2() failed with %lu\n", Status);
        goto Exit;
    }

    //
    // Clean up the payload descriptor
    //
    Status = TdhCleanupPayloadEventFilterDescriptor(&FilterDescriptor);
    if (Status != ERROR_SUCCESS) {
        printf("TdhCleanupPayloadEventFilterDescriptor() failed with %lu\n", Status);
        goto Exit;
    }

    //
    // Collect trace for 30 seconds
    //
    Sleep(30 * 1000);

Exit:

    //
    // Stop tracing.
    //
    if (TraceStarted != FALSE) {
        Status = ControlTraceW(SessionHandle, NULL, TraceProperties, EVENT_TRACE_CONTROL_STOP);
        if (Status != ERROR_SUCCESS) {
            printf("StopTrace() failed with %lu\n", Status);
        }
    }

    if (TraceProperties != NULL) {
        FreeTraceProperties(TraceProperties);
    }

    TdhUnloadManifest((PWSTR)PATH_TO_MANIFEST_FILE);

    return Status;
}
```

## -see-also

[StartTrace](/windows/win32/api/evntrace/nf-evntrace-starttracea)

[ControlTrace](/windows/win32/api/evntrace/nf-evntrace-controltracea)

[EnableCallback](/windows/win32/api/evntprov/nc-evntprov-penablecallback)

[ENABLE_TRACE_PARAMETERS](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters)

[EVENT_FILTER_DESCRIPTOR](/windows/desktop/api/evntprov/ns-evntprov-event_filter_descriptor)
