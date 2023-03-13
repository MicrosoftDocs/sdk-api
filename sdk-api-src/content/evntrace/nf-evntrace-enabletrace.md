---
UID: NF:evntrace.EnableTrace
title: EnableTrace function (evntrace.h)
description:
  A trace session controller calls EnableTrace to configure how an ETW event
  provider logs events to a trace session. The EnableTraceEx2 function
  supersedes this function.
helpviewer_keywords:
  [
    "EnableTrace",
    "EnableTrace function [ETW]",
    "TRACE_LEVEL_CRITICAL",
    "TRACE_LEVEL_ERROR",
    "TRACE_LEVEL_INFORMATION",
    "TRACE_LEVEL_VERBOSE",
    "TRACE_LEVEL_WARNING",
    "_evt_enabletrace",
    "base.enabletrace",
    "etw.enabletrace",
    "evntrace/EnableTrace",
  ]
old-location: etw\enabletrace.htm
tech.root: ETW
ms.assetid: d75f18e1-e5fa-4039-bb74-76dea334b0fd
ms.date: 12/05/2018
ms.keywords:
  EnableTrace, EnableTrace function [ETW], TRACE_LEVEL_CRITICAL,
  TRACE_LEVEL_ERROR, TRACE_LEVEL_INFORMATION, TRACE_LEVEL_VERBOSE,
  TRACE_LEVEL_WARNING, _evt_enabletrace, base.enabletrace, etw.enabletrace,
  evntrace/EnableTrace
req.header: evntrace.h
req.include-header:
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
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
  - EnableTrace
  - evntrace/EnableTrace
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
  - EnableTrace
---

# EnableTrace function

## -description

A trace session controller calls **EnableTrace** to configure how an ETW event
provider logs events to a trace session.

This function is obsolete. The
[EnableTraceEx2](/windows/desktop/ETW/enabletraceex2) function supersedes this
function.

## -parameters

### -param Enable [in]

Set to 1 to enable receiving events from the provider or to adjust the settings
used when receiving events from the provider (e.g. to change level and
keywords). Set to 0 to disable receiving events from the provider.

### -param EnableFlag [in]

32-bit bitmask of keywords that determine the categories of events that you want
the provider to write. The provider typically writes an event if the event's
keyword bits match **any** of the bits set in this value or if the event has no
keyword bits set, in addition to meeting the _EnableLevel_ critera.

> [!Note]
> EventRegister-based providers support 64-bit keywords. Use
> **EnableTraceEx2** to enable providers using a 64-bit _MatchAnyKeyword_ mask.

### -param EnableLevel [in]

A value that indicates the maximum level of events that you want the provider to
write. The provider typically writes an event if the event's level is less than
or equal to this value, in addition to meeting the _EnableFlag_ criteria.

This value should be in the range 1 to 255. Microsoft defines the semantics of
levels 1-5 as shown below. Lower values indicate more-severe events. Each value
of _EnableLevel_ enables the specified level and all more-severe levels. For
example, if you specify `TRACE_LEVEL_WARNING`, your consumer will receive
warning, error, and critical events.

| Value                           | Meaning                                    |
| ------------------------------- | ------------------------------------------ |
| **TRACE_LEVEL_CRITICAL** (1)    | Abnormal exit or termination events        |
| **TRACE_LEVEL_ERROR** (2)       | Severe error events                        |
| **TRACE_LEVEL_WARNING** (3)     | Warning events such as allocation failures |
| **TRACE_LEVEL_INFORMATION** (4) | Non-error informational events             |
| **TRACE_LEVEL_VERBOSE** (5)     | Detailed diagnostic events                 |

The `TRACE_LEVEL` constants are defined in _evntrace.h_. Equivalent
`WINMETA_LEVEL` constants are defined in _winmeta.h_.

### -param ControlGuid [in]

The control GUID (provider ID) of the event provider that you want to enable or
disable.

### -param TraceHandle [in]

Handle of the event tracing session for which you are configuring the provider.
The [StartTrace](/windows/win32/api/evntrace/nf-evntrace-starttracea) function
returns this handle when a new trace is started. To obtain the handle of an
existing trace, use
[ControlTrace](/windows/win32/api/evntrace/nf-evntrace-controltracew) to query
the trace properties based on the trace's name and then get the handle from the
**Wnode.HistoricalContext** field of the returned `EVENT_TRACE_PROPERTIES` data.

## -returns

If the function is successful, the return value is ERROR_SUCCESS.

If the function fails, the return value is one of the
[system error codes](/windows/win32/debug/system-error-codes). The following
are some common errors and their causes.

- **ERROR_INVALID_PARAMETER**

  One of the following is true:

  - _ControlGuid_ is **NULL**.
  - _TraceHandle_ is **NULL**.

- **ERROR_INVALID_FUNCTION**

  You cannot change the enable flags and level when the provider is not
  registered.

- **ERROR_WMI_GUID_NOT_FOUND**

  The provider is not registered. Occurs when KB307331 or Windows 2000 Service
  Pack 4 is installed and the provider is not registered. To avoid this error,
  the provider must first be registered.

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

The following two function calls are equivalent:

```C
// Obsolete:
Status = EnableTrace(
    Enable,
    EnableFlag,
    EnableLevel,
    ControlGuid,
    TraceHandle);

// Updated equivalent code:
Status = EnableTraceEx2(
    TraceHandle,
    ControlGuid,
    Enable,      // ControlCode
    EnableLevel,
    EnableFlag,  // MatchAnyKeyword
    0,           // MatchAllKeyword
    0,           // Timeout
    NULL);       // EnableParameters
```

For additional details on the semantics of configuring providers for a session,
refer to the documentation for
[EnableTraceEx2](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2).

## -see-also

[StartTrace](/windows/desktop/ETW/starttrace)

[EnableTraceEx2](/windows/desktop/ETW/enabletraceex2)
