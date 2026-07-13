---
UID: NC:evntprov.PENABLECALLBACK
title: PENABLECALLBACK (evntprov.h)
description:
  ETW event providers optionally define an EnableCallback function to receive
  configuration change notifications. The PENABLECALLBACK type defines a pointer
  to this callback function. EnableCallback is a placeholder for the
  application-defined function name.
helpviewer_keywords:
  [
    "EVENT_CONTROL_CODE_CAPTURE_STATE",
    "EVENT_CONTROL_CODE_DISABLE_PROVIDER",
    "EVENT_CONTROL_CODE_ENABLE_PROVIDER",
    "PENABLECALLBACK",
    "PENABLECALLBACK callback",
    "PENABLECALLBACK callback function [ETW]",
    "base.enablecallback",
    "etw.enablecallback",
    "evntprov/PENABLECALLBACK",
  ]
old-location: etw\enablecallback.htm
tech.root: ETW
ms.assetid: f339323e-9da9-495f-aac5-f44969a018eb
ms.date: 12/05/2018
ms.keywords:
  EVENT_CONTROL_CODE_CAPTURE_STATE, EVENT_CONTROL_CODE_DISABLE_PROVIDER,
  EVENT_CONTROL_CODE_ENABLE_PROVIDER, PENABLECALLBACK, PENABLECALLBACK callback,
  PENABLECALLBACK callback function [ETW], base.enablecallback,
  etw.enablecallback, evntprov/PENABLECALLBACK
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
req.typenames:
req.redist:
ms.custom: 19H1
f1_keywords:
  - PENABLECALLBACK
  - evntprov/PENABLECALLBACK
dev_langs:
  - c++
topic_type:
  - APIRef
  - kbSyntax
api_type:
  - UserDefined
api_location:
  - Evntprov.h
api_name:
  - PENABLECALLBACK
---

## -description

ETW event providers optionally define an **EnableCallback** function to receive
configuration change notifications. The **PENABLECALLBACK** type defines a
pointer to this callback function. **EnableCallback** is a placeholder for the
application-defined function name.

## -parameters

### -param SourceId [in]

GUID specified by the caller that is enabling or disabling the provider.

The value comes from the _SourceId_ parameter of
[EnableTraceEx](/windows/win32/api/evntrace/nf-evntrace-enabletraceex) or the
_SourceId_ field of the
[ENABLE_TRACE_PARAMETERS](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters)
that is passed to
[EnableTraceEx2](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2).

> [!Note]
> The _SourceId_ is the value the session specified in the call to the
> EnableTraceEx or EnableTraceEx2 API. It may or may not be the same as the
> session's GUID.

_SourceId_ will be set to **GUID_NULL** in several scenarios where the
notification does not have a source identifier. For example, this can occur when
a trace session enabled the provider before the provider started, when the
provider is stopping, or when a trace controller calls an EnableTrace API
without specifying a _SourceId_.

### -param IsEnabled [in]

Indicates the ControlCode corresponding to this notification. This can be one of
the following values:

| Value                                       | Meaning                                                                                                                                               |
| ------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------- |
| **EVENT_CONTROL_CODE_DISABLE_PROVIDER** (0) | No sessions have enabled the provider.                                                                                                                |
| **EVENT_CONTROL_CODE_ENABLE_PROVIDER** (1)  | One or more sessions have enabled the provider.                                                                                                       |
| **EVENT_CONTROL_CODE_CAPTURE_STATE** (2)    | A session is requesting that the provider log its state information. The provider will typically respond by writing events containing provider state. |

> [!Note]
> The value of _IsEnabled_ may not be the same as the _ControlCode_ passed to
> the **EnableTrace** API that triggered this event. For example, if two
> sessions have enabled this provider and one session disables this provider by
> calling `EnableTraceEx2(..., EVENT_CONTROL_CODE_DISABLE_PROVIDER, ...)`, the
> provider would receive a notification with _IsEnabled_ set to
> `EVENT_CONTROL_CODE_ENABLE_PROVIDER` because the provider is still enabled by
> the other session.

After receiving a **DISABLE_PROVIDER** notification, a provider may optimize its
performance by disabling all events. After receiving an **ENABLE_PROVIDER**
notification, a provider should enable writing events. It may also optimize its
performance by recording the values of the Level, MatchAnyKeyword, and
MatchAllKeyword filters, and then only writing the events that pass the filters
(as described in _remarks_). After receiving a **CAPTURE_STATE** notification, a
provider may take whatever action seems appropriate, typically writing events
that describe the component's configuration or state.

A provider should ignore notifications with _IsEnabled_ values that it does not
recognize or support.

### -param Level [in]

A value that specifies the verbosity of the events that the provider should
write. When invoked with the control code
**EVENT_CONTROL_CODE_ENABLE_PROVIDER**, the provider should record the _Level_
value and should subsequently skip events where the event's verbosity level is
greater than the recorded _Level_, i.e. an event should only be written if

`eventDescriptor.Level <= recorded.Level`

The _Level_ in the notification is the maximum of the levels specified by trace
controllers in calls to **EnableTrace**, **EnableTraceEx**, or
**EnableTraceEx2** using this event provider's GUID. In other words, if multiple
sessions are recording events from this event provider at different verbosity
levels, the _Level_ parameter for the **EnableCallback** notification will be
set to the highest (most verbose) of the levels.

### -param MatchAnyKeyword [in]

A bitmask value that specifies categories of events that the provider should
write. When invoked with the control code
**EVENT_CONTROL_CODE_ENABLE_PROVIDER**, the provider should record the
_MatchAnyKeyword_ value and should subsequently skip events where the event's
keyword is nonzero and does not have any of the bits from the recorded
_MatchAnyKeyword_, i.e. an event should only be written if

`eventDescriptor.Keyword == 0 || (eventDescriptor.Keyword & recorded.MatchAnyKeyword) != 0`

The _MatchAnyKeyword_ in the notification is the union (OR) of the
match-any-keywords (enable flags) specified by trace controllers in calls to
**EnableTrace**, **EnableTraceEx**, and **EnableTraceEx2** for this event
provider's GUID. In other words, if multiple sessions are recording events from
this event provider with different match-any-keyword filters, the
_MatchAnyKeyword_ parameter for the **EnableCallback** notification will be set
to the bitwise-`OR` of the match-any-keyword filters of the sessions.

### -param MatchAllKeyword

A bitmask value that specifies categories of events that the provider should
write. When notified with the control code
**EVENT_CONTROL_CODE_ENABLE_PROVIDER**, the provider should record the
_MatchAllKeyword_ value and should subsequently skip events where the event's
keyword is nonzero and does not have all of the bits from the recorded
_MatchAllKeyword_, i.e. an event should only be written if

`eventDescriptor.Keyword == 0 || (eventDescriptor.Keyword & recorded.MatchAllKeyword) == recorded.MatchAllKeyword`

The _MatchAllKeyword_ in the notification is the disjunction (AND) of the
match-all-keywords specified by trace controllers in calls to **EnableTraceEx**
and **EnableTraceEx2** for this event provider's GUID. In other words, if
multiple sessions are recording events from this event provider with different
match-all-keyword filters, the _MatchAllKeyword_ parameter for the
**EnableCallback** notification will be set to the bitwise-`AND` of the
match-all-keyword filters of the sessions.

### -param FilterData [in, optional]

A pointer to an
[EVENT_FILTER_DESCRIPTOR](/windows/win32/api/evntprov/ns-evntprov-event_filter_descriptor)
with filter data for the event provider.

Each session can specify only one filter. The filter descriptor in the callback
notification will contain one filter from each session that specified filter
data when enabling the provider.

The filter data is valid only within the callback. Providers should make a local
copy of the data if the data will be needed after the callback returns.

### -param CallbackContext [in, optional]

Context for the callback. This is the value of the _CallbackContext_ parameter
that was used when the event provider called
[EventRegister](/windows/win32/api/evntprov/nf-evntprov-eventregister).

## -remarks

ETW event providers that need configuration change notifications should provide
a pointer to their **EnableCallback** implementation when they register via
[EventRegister](/windows/win32/api/evntprov/nf-evntprov-eventregister). ETW will
invoke the provider's **EnableCallback** function when a change is made to the
configuration of a trace session that involves the provider. For example, when a
trace session controller configures a trace via
[EnableTraceEx2](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2) or
stops a trace via
[ControlTrace](/windows/win32/api/evntrace/nf-evntrace-controltracew), ETW will
call the provider's **EnableCallback** function with the resulting updated
configuration.

> [!Note]
> Most event providers will not implement **EnableCallback** directly. Instead,
> most event providers are implemented using an ETW framework that provides its
> own **EnableCallback** implementation and wraps the calls to
> **EventRegister**, **EventWrite**, and **EventUnregister**. For example, you
> might
> [write an event manifest](/windows/win32/etw/writing-manifest-based-events)
> and then use the
> [Message Compiler](/windows/win32/wes/message-compiler--mc-exe-) to generate
> C/C++ code for the events, or you might use
> [TraceLogging](/windows/win32/tracelogging/trace-logging-portal) to avoid the
> need for a manifest. The ETW framework typically implements an
> **EnableCallback** function that records the notification's `Level`,
> `MatchAnyKeyword`, and `MatchAllKeyword` values, and the framework
> automatically uses the recorded values to filter events. The ETW framework
> usually supports invoking a user-provided callback if the user requires custom
> notification handling. For example,
> [TraceLoggingProvider.h](/windows/win32/api/traceloggingprovider/) allows a
> notification callback to be specified via
> [TraceLoggingRegisterEx](/windows/win32/api/traceloggingprovider/nf-traceloggingprovider-traceloggingregisterex).

> [!Important]
> The provider's **EnableCallback** function should be as simple as
> possible. It should record the required information and return quickly. A
> long-running callback function can cause delays in ETW session control APIs such
> as **EnableTraceEx2** or **ControlTrace**. The callback function must not do
> anything that requires the process's loader lock, i.e. it must not directly or
> indirectly call **LoadLibrary** or **FreeLibrary**. The callback function must
> not block on locks. The callback function may cause a deadlock if it blocks on
> locks or if it invokes any ETW session control APIs such as **StartTrace**,
> **ControlTrace**, or **EnableTrace**.

The notification callback allows the event provider to run more efficiently
because the provider can perform its own tracking of the level, keywords, and
other filters. By tracking the filters, the provider can efficiently skip events
that are not enabled (i.e. the provider does not need to prepare the event data
or call **EventWrite** for events that are not needed by any trace sessions).

Note that filter tracking is not required for correct operation of a provider:
ETW provides
[EventEnabled](/windows/desktop/api/evntprov/nf-evntprov-eventenabled) and
[EventProviderEnabled](/windows/desktop/api/evntprov/nf-evntprov-eventproviderenabled)
functions that a provider can use, and the ETW **EventWrite** APIs will silently
ignore any disabled events. However, provider-implemented filter tracking can be
more efficient than calls to **EventEnabled** or **EventProviderEnabled**.

The notification callback also allows the provider to handle "capture-state"
requests from trace sessions. Capture-state requests are typically sent by a
trace session when it begins recording events from a provider. If capture-state
is supported by a provider, it might respond to the capture-state request by
logging state information, e.g. configuration information or summary statistics
regarding the component's operation prior to the request.

The _Level_ value that ETW passes to the callback is the highest (most verbose)
level value specified for this event provider by any running trace session. For
example, if session A has enabled this provider for warning (level 3) events and
then session B enables the provider for critical (level 1) events, the _Level_
value for the callback will be 3, not 1.

Similarly, the _MatchAnyKeyword_ and _MatchAllKeyword_ values are composite
values computed from the configuration of all sessions that have enabled the
event provider. _MatchAnyKeyword_ is the OR of the EnableFlags/MatchAnyKeyword
settings of the sessions. _MatchAllKeyword_ is the AND of the MatchAllKeyword
settings of the sessions.

If the provider's **EnableCallback** function has captured the provider's
Enabled, Level, MatchAnyKeyword, and MatchAllKeyword state, the provider can
determine whether an event should be written using a function like the
following:

```c
BOOL MyProviderEventEnabled(
    _In_ const MY_PROVIDER_STATE* pProvider,
    _In_ const EVENT_DESCRIPTOR* pEvent)
{
    return
        pProvider->Enabled &&
        pEvent->Level <= pProvider->Level &&
        (pEvent->Keyword == 0 || (
            (pEvent->Keyword & pProvider->MatchAnyKeyword) != 0 &&
            (pEvent->Keyword & pProvider->MatchAllKeyword) == pProvider->MatchAllKeyword
        ));
}
```

## -see-also

[EventRegister](/windows/win32/api/evntprov/nf-evntprov-eventregister)

[EnableTrace](/windows/win32/api/evntrace/nf-evntrace-enabletrace)

[EnableTraceEx2](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2)
