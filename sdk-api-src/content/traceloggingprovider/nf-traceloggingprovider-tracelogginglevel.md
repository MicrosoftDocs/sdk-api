---
UID: NF:traceloggingprovider.TraceLoggingLevel
title: TraceLoggingLevel macro (traceloggingprovider.h)
description: TraceLogging wrapper macro that sets the level for the event
helpviewer_keywords:
  [
    "TraceLoggingLevel",
    "TraceLoggingLevel macro",
    "tracelogging.tracelogginglevel",
    "traceloggingprovider/TraceLoggingLevel",
  ]
old-location: tracelogging\tracelogginglevel.htm
tech.root: tracelogging
ms.assetid: 280EEFC4-EC84-4FAA-B14B-CBC5F0E0EA5D
ms.date: 07/01/2025
ms.keywords:
  TraceLoggingLevel, TraceLoggingLevel macro, tracelogging.tracelogginglevel,
  traceloggingprovider/TraceLoggingLevel
req.header: traceloggingprovider.h
req.include-header:
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
  - TraceLoggingLevel
  - traceloggingprovider/TraceLoggingLevel
dev_langs:
  - c++
topic_type:
  - APIRef
  - kbSyntax
api_type:
  - HeaderDef
api_location:
  - traceloggingprovider.h
api_name:
  - TraceLoggingLevel
---

# TraceLoggingLevel macro

## -syntax

```cpp
void TraceLoggingLevel(
  [in]  UINT eventLevel
);
```

## -description

[TraceLogging wrapper macro](/windows/desktop/tracelogging/tracelogging-wrapper-macros)
that sets the level for the event.

## -parameters

### -param eventLevel [in]

An 8-bit number used to describe an event's severity or importance. This value
must be a compile-time constant in the range 0 to 255. If no
**TraceLoggingLevel** arguments are provided to a **TraceLoggingWrite** call,
the event's level will default to 5 (WINEVENT_LEVEL_VERBOSE).

> [!IMPORTANT]
> ProviderId, Level and Keyword are the primary means for filtering
> events. Other kinds of filtering are possible but have much higher overhead.
> Always assign a meaningful non-zero level and keyword to every event.

See [EVENT_DESCRIPTOR](../evntprov/ns-evntprov-event_descriptor.md) for details
about the event level.

## -remarks

`TraceLoggingLevel(eventLevel)` can be used as a parameter to an invocation of a
[TraceLoggingWrite](./nf-traceloggingprovider-traceloggingwrite.md) macro to set
the event's level. Event level is a primary means for filtering events. Always
assign a meaningful (non-zero) level to every event.

If no **TraceLoggingLevel** macros are provided to a **TraceLoggingWrite** call,
the event's default level is 5 (WINEVENT_LEVEL_VERBOSE). If multiple
**TraceLoggingLevel** macros are provided, the last value is used.

Level values 0 through 5 are defined by Microsoft (see `evntrace.h` and
`winmeta.h`). Level values 6 through 15 are reserved for future definition by
Microsoft. Level values 16 through 255 can be defined by the event provider.

| Value              | Semantics                                                                     |
| ------------------ | ----------------------------------------------------------------------------- |
| **LOG_ALWAYS** (0) | Event bypasses level-based event filtering. Events should not use this level. |
| **CRITICAL** (1)   | Critical error                                                                |
| **ERROR** (2)      | Error                                                                         |
| **WARNING** (3)    | Warning                                                                       |
| **INFO** (4)       | Informational                                                                 |
| **VERBOSE** (5)    | Verbose                                                                       |

Event collection sessions can set a level filter, meaning that the session will
only accept events where `eventDescriptor.Level <= session.LevelFilter`. Note
that events with a level of 0 will bypass level-based filtering.

### Examples

```c
TraceLoggingWrite(
    g_hMyProvider,
    "MyWarningEventName",
    TraceLoggingLevel(WINEVENT_LEVEL_WARNING), // Levels defined in <winmeta.h>
    TraceLoggingKeyword(MyNetworkingKeyword), // Provider-defined keyword
    TraceLoggingHResult(errorCode, "Error"));
```

## -see-also

[EVENT_DESCRIPTOR](../evntprov/ns-evntprov-event_descriptor.md)

[TraceLoggingWrite](./nf-traceloggingprovider-traceloggingwrite.md)

[TraceLogging wrapper macros](/windows/desktop/tracelogging/tracelogging-wrapper-macros)
