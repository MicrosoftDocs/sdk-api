---
UID: NF:evntrace.EnableTraceEx
title: EnableTraceEx function (evntrace.h)
description:
  A trace session controller calls EnableTraceEx to configure how an ETW event
  provider logs events to a trace session. The EnableTraceEx2 function
  supersedes this function.
helpviewer_keywords:
  [
    "EVENT_ENABLE_PROPERTY_SID",
    "EVENT_ENABLE_PROPERTY_TS_ID",
    "EnableTraceEx",
    "EnableTraceEx function [ETW]",
    "TRACE_LEVEL_CRITICAL",
    "TRACE_LEVEL_ERROR",
    "TRACE_LEVEL_INFORMATION",
    "TRACE_LEVEL_VERBOSE",
    "TRACE_LEVEL_WARNING",
    "base.enabletraceex_func",
    "etw.enabletraceex_func",
    "evntrace/EnableTraceEx",
  ]
old-location: etw\enabletraceex_func.htm
tech.root: ETW
ms.assetid: 1c675bf7-f292-49b1-8b60-720499a497fd
ms.date: 12/05/2018
ms.keywords:
  EVENT_ENABLE_PROPERTY_SID, EVENT_ENABLE_PROPERTY_TS_ID, EnableTraceEx,
  EnableTraceEx function [ETW], TRACE_LEVEL_CRITICAL, TRACE_LEVEL_ERROR,
  TRACE_LEVEL_INFORMATION, TRACE_LEVEL_VERBOSE, TRACE_LEVEL_WARNING,
  base.enabletraceex_func, etw.enabletraceex_func, evntrace/EnableTraceEx
req.header: evntrace.h
req.include-header:
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver:
req.umdf-ver:
req.ddi-compliance:
req.unicode-ansi:
req.idl:
req.max-support:
req.namespace:
req.assembly:
req.type-library:
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql:
targetos: Windows
req.typenames:
req.redist:
ms.custom: 19H1
f1_keywords:
  - EnableTraceEx
  - evntrace/EnableTraceEx
dev_langs:
  - c++
topic_type:
  - APIRef
  - kbSyntax
api_type:
  - DllExport
api_location:
  - Advapi32.dll
  - API-MS-Win-eventing-Legacy-l1-1-0.dll
  - advapi32legacy.dll
api_name:
  - EnableTraceEx
---

# EnableTraceEx function

## -description

A trace session controller calls **EnableTraceEx** to configure how an ETW event
provider logs events to a trace session.

This function is obsolete. The
[EnableTraceEx2](/windows/desktop/ETW/enabletraceex2) function supersedes this
function.

## -parameters

### -param ProviderId [in]

The provider ID (control GUID) of the event provider that you want to configure.

### -param SourceId [in, optional]

A GUID that can uniquely identify the source of this configuration request, or
**NULL** if no source identity is needed (equivalent to setting _SourceId_ to
`&GUID_NULL`). If specified, this value is used as the _SourceId_ parameter when
invoking the provider's
[EnableCallback](/windows/win32/api/evntprov/nc-evntprov-penablecallback).

> [!Note]
> There is not always a direct mapping between a call to **EnableTrace**
> and a corresponding call to the provider's **EnableCallback**. For example, if
> **EnableTrace** is called for a provider that has not yet been registered, the
> call to **EnableCallback** will be deferred until the registration occurs, and
> if a trace consumer session is stopped, ETW will invoke **EnableCallback**
> even though there was no corresponding call to **EnableTrace**. In such cases,
> **EnableTrace** will be invoked with _SourceId_ set to **GUID_NULL**.

### -param TraceHandle [in]

Handle of the event tracing session for which you are configuring the provider.
The [StartTrace](/windows/win32/api/evntrace/nf-evntrace-starttracea) function
returns this handle when a new trace is started. To obtain the handle of an
existing trace, use
[ControlTrace](/windows/win32/api/evntrace/nf-evntrace-controltracew) to query
the trace properties based on the trace's name and then get the handle from the
**Wnode.HistoricalContext** field of the returned `EVENT_TRACE_PROPERTIES` data.

### -param IsEnabled [in]

Set to 1 to enable receiving events from the provider or to adjust the settings
used when receiving events from the provider (e.g. to change level and
keywords). Set to 0 to disable receiving events from the provider.

### -param Level [in]

A value that indicates the maximum level of events that you want the provider to
write. The provider typically writes an event if the event's level is less than
or equal to this value, in addition to meeting the _MatchAnyKeyword_ and
_MatchAllKeyword_ criteria.

Microsoft defines the semantics of levels 1-5 as shown below. Lower values
indicate more-severe events. Each value of _EnableLevel_ enables the specified
level and all more-severe levels. For example, if you specify
`TRACE_LEVEL_WARNING`, your consumer will receive warning, error, and critical
events.

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

### -param EnableProperty [in]

Flags specifying special behaviors that the ETW runtime should enable when
collecting events from this provider. To enable special behaviors, specify one
or more of the following flags. Otherwise, set _EnableProperty_ to 0.

> [!Note]
> Several of these flags indicate that ETW should include extra
> information into each event. The data is written to the
> [extended data item](/windows/win32/api/evntcons/ns-evntcons-event_header_extended_data_item)
> section of the event.

| Value                                      | Meaning                                                                 |
| ------------------------------------------ | ----------------------------------------------------------------------- |
| **EVENT_ENABLE_PROPERTY_SID**              | Include the security identifier (SID) of the user in the extended data. |
| **EVENT_ENABLE_PROPERTY_TS_ID**            | Include the terminal session identifier in the extended data.           |
| **EVENT_ENABLE_PROPERTY_IGNORE_KEYWORD_0** | The trace session should not record events that have a keyword of 0.    |

### -param EnableFilterDesc [in, optional]

An
[EVENT_FILTER_DESCRIPTOR](/windows/desktop/api/evntprov/ns-evntprov-event_filter_descriptor)
structure that points to the filter data. The provider uses this to filter data
to prevent events that do not match the filter criteria from being written to
the session. The provider determines the layout of the data and how it applies
the filter to the event's data. A session can pass only one filter to the
provider.

A session can call the
[TdhEnumerateProviderFilters](/windows/desktop/api/tdh/nf-tdh-tdhenumerateproviderfilters)
function to look up the filters for which a provider has registered support.

## -returns

If the function is successful, the return value is ERROR_SUCCESS.

If the function fails, the return value is one of the
[system error codes](/windows/win32/debug/system-error-codes). The following
are some common errors and their causes.

- **ERROR_INVALID_PARAMETER**

  One of the following is true:

  - _ProviderId_ is **NULL**.
  - _TraceHandle_ is **NULL**.

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

This function is obsolete. For additional functionality, new code should use
[EnableTraceEx2](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2).

In most cases, a call to **EnableTraceEx** can be converted to
**EnableTraceEx2** as follows:

```C
// Obsolete:
Status =
EnableTraceEx(
    ProviderId,
    NULL,           // SourceId
    TraceHandle,
    IsEnabled,
    Level,
    MatchAnyKeyword,
    MatchAllKeyword,
    0,              // EnableProperty
    NULL);          // EnableFilterDesc

// Updated equivalent code:
Status = EnableTraceEx2(
    TraceHandle,
    ProviderId,
    IsEnabled,
    Level,
    MatchAnyKeyword,
    MatchAllKeyword,
    0,              // Timeout
    NULL);          // EnableParameters
```

In more complex scenarios, a call to **EnableTraceEx** can be converted to
**EnableTraceEx2** as follows:

```C
// Obsolete:
Status =
EnableTraceEx(
    ProviderId,
    SourceId,
    TraceHandle,
    IsEnabled,
    Level,
    MatchAnyKeyword,
    MatchAllKeyword,
    EnableProperty,
    EnableFilterDesc);

// Updated equivalent code:
ENABLE_TRACE_PARAMETERS EnableParameters = {
    ENABLE_TRACE_PARAMETERS_VERSION_2,
    EnableProperty,
    0,                 // ControlFlags
    SourceId ? *SourceId : GUID_NULL,
    EnableFilterDesc,
    EnableFilterDesc ? 1 : 0 };
Status = EnableTraceEx2(
    TraceHandle,
    ProviderId,
    IsEnabled,
    Level,
    MatchAnyKeyword,
    MatchAllKeyword,
    0,                 // Timeout
    &EnableParameters);
```

For additional details on the semantics of configuring providers for a session,
refer to the documentation for
[EnableTraceEx2](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2).

## -see-also

[StartTrace](/windows/desktop/ETW/starttrace)

[EnableTraceEx2](/windows/desktop/ETW/enabletraceex2)
