---
UID: NF:traceloggingprovider.TraceLoggingEventTag
title: TraceLoggingEventTag macro (traceloggingprovider.h)
description: TraceLogging wrapper macro that sets the event tag for the event.
helpviewer_keywords:
  [
    "TraceLoggingEventTag",
    "TraceLoggingEventTag macro",
    "tracelogging.traceloggingeventtag",
    "traceloggingprovider/TraceLoggingEventTag",
  ]
old-location: tracelogging\traceloggingeventtag.htm
tech.root: tracelogging
ms.assetid: D7BD0AC7-2330-4DE7-8C46-CF210B102704
ms.date: 07/01/2025
ms.keywords:
  TraceLoggingEventTag, TraceLoggingEventTag macro,
  tracelogging.traceloggingeventtag, traceloggingprovider/TraceLoggingEventTag
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
  - TraceLoggingEventTag
  - traceloggingprovider/TraceLoggingEventTag
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
  - TraceLoggingEventTag
---

# TraceLoggingEventTag macro

## -syntax

```cpp
void TraceLoggingEventTag(
  [in]  UINT eventTag
);
```

## -description

[TraceLogging wrapper macro](/windows/desktop/tracelogging/tracelogging-wrapper-macros)
that sets the event tag for the event.

## -parameters

### -param eventTag [in]

This is a compile-time constant specifying the event tag value.

In C++, this can be any value in the range 0 through 0x0FFFFFFF.

In C, this can be any value in the range 0 through 0x0FFFA000 with the low 14
bits set to 0.

## -remarks

`TraceLoggingEventTag(eventTag)` can be used as a parameter to an invocation of
a [TraceLoggingWrite](./nf-traceloggingprovider-traceloggingwrite.md) macro to
set the event's tag.

The semantics of the tag are defined by the event consumer. During event
processing, the tag value can be retrieved from the
[TRACE_EVENT_INFO](../tdh/ns-tdh-trace_event_info.md) Tags field.

The TraceLogging schema convention encodes tags as 28-bit field by using a chain
of up to four bytes with the upper-most bit used as a 'chain' bit (4 bytes \* 7
usable bits per byte = 28 bits). Data is encoded most-significant byte first. In
C, [TraceLoggingWrite](./nf-traceloggingprovider-traceloggingwrite.md) is
limited to a 2-byte encoding for the tag, so the low 14 bits of the tag must
be 0.

If no TraceLoggingEventTag parameters are provided for an event, no tag is
transmitted for the event and the event will have a tag of 0. If multiple
TraceLoggingEventTag parameters are provided, the tag values are OR'ed together.

## -see-also

[TraceLoggingWrite](./nf-traceloggingprovider-traceloggingwrite.md)

[TraceLogging wrapper macros](/windows/desktop/tracelogging/tracelogging-wrapper-macros)

[TRACE_EVENT_INFO](../tdh/ns-tdh-trace_event_info.md)
