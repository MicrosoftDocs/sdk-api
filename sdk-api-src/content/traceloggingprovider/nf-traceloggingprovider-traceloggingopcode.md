---
UID: NF:traceloggingprovider.TraceLoggingOpcode
title: TraceLoggingOpcode macro (traceloggingprovider.h)
description: TraceLogging wrapper macro that sets the opcode for the event
helpviewer_keywords:
  [
    "TraceLoggingOpcode",
    "TraceLoggingOpcode macro",
    "tracelogging.traceloggingopcode",
    "traceloggingprovider/TraceLoggingOpcode",
  ]
old-location: tracelogging\traceloggingopcode.htm
tech.root: tracelogging
ms.assetid: 8D1459CE-51A8-49A8-A30B-EA8D87E822C3
ms.date: 07/01/2025
ms.keywords:
  TraceLoggingOpcode, TraceLoggingOpcode macro, tracelogging.traceloggingopcode,
  traceloggingprovider/TraceLoggingOpcode
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
  - TraceLoggingOpcode
  - traceloggingprovider/TraceLoggingOpcode
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
  - TraceLoggingOpcode
---

# TraceLoggingOpcode macro

## -syntax

```cpp
void TraceLoggingOpcode(
  [in]  UINT eventOpcode
);
```

## -description

[TraceLogging wrapper macro](/windows/desktop/tracelogging/tracelogging-wrapper-macros)
that sets the opcode for the event.

## -parameters

### -param eventOpcode [in]

An 8-bit number used to mark events with special semantics. This value must be a
compile-time constant in the range 0 to 255.

The opcode will be used by trace decoders to organize and correlate events.
Globally-recognized opcode values are defined in `winmeta.h`. Most events use 0
(WINEVENT_OPCODE_INFO) to indicate that the event has no special semantics.
Opcode values 10 through 239 can be given user-defined semantics.

See [EVENT_DESCRIPTOR](../evntprov/ns-evntprov-event_descriptor.md) for details
about the event opcode.

## -remarks

`TraceLoggingOpcode(eventOpcode)` can be used as a parameter to an invocation of
a [TraceLoggingWrite](./nf-traceloggingprovider-traceloggingwrite.md) macro to
set the event's opcode.

If no **TraceLoggingOpcode** macros are provided to a **TraceLoggingWrite**
call, the event's default opcode is 0 (WINEVENT_OPCODE_INFO). If multiple
**TraceLoggingOpcode** macros are provided, the last value is used.

Opcodes WINEVENT_OPCODE_START (1) and WINEVENT_OPCODE_STOP (2) are used to
indicate the beginning and end of ETW activities as follows:

1. Generate an activity ID that is unique within the trace, typically using
   [EventActivityIdControl](../evntprov/nf-evntprov-eventactivityidcontrol.md)
   or [UuidCreate](../rpcdce/nf-rpcdce-uuidcreate.md).
2. Write a start event with opcode = START, activity ID = the generated activity
   ID, and related activity ID = the parent activity ID (or NULL if no parent
   activity ID).
3. Write any number of activity information events with opcode = INFO, activity
   ID = the generated activity ID.
4. Write a stop event with opcode = STOP, activity ID = the generated activity
   ID.

Trace decoding tools will then be able to organize these events into groups
based on their activity IDs.

## -see-also

[EVENT_DESCRIPTOR](../evntprov/ns-evntprov-event_descriptor.md)

[EventActivityIdControl](../evntprov/nf-evntprov-eventactivityidcontrol.md)

[TraceLoggingWrite](./nf-traceloggingprovider-traceloggingwrite.md)

[TraceLogging wrapper macros](/windows/desktop/tracelogging/tracelogging-wrapper-macros)
