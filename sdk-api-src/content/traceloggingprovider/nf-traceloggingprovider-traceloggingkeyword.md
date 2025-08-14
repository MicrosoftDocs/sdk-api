---
UID: NF:traceloggingprovider.TraceLoggingKeyword
title: TraceLoggingKeyword macro (traceloggingprovider.h)
description: TraceLogging wrapper macro that sets the keyword for the event.
helpviewer_keywords:
  [
    "TraceLoggingKeyword",
    "TraceLoggingKeyword macro",
    "tracelogging.traceloggingkeyword",
    "traceloggingprovider/TraceLoggingKeyword",
  ]
old-location: tracelogging\traceloggingkeyword.htm
tech.root: tracelogging
ms.assetid: 4837DCE3-929F-458B-95E1-8720FD3E9FFA
ms.date: 07/01/2025
ms.keywords:
  TraceLoggingKeyword, TraceLoggingKeyword macro,
  tracelogging.traceloggingkeyword, traceloggingprovider/TraceLoggingKeyword
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
  - TraceLoggingKeyword
  - traceloggingprovider/TraceLoggingKeyword
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
  - TraceLoggingKeyword
---

# TraceLoggingKeyword macro

## -syntax

```cpp
void TraceLoggingKeyword(
  [in]  UINT64 eventKeyword
);
```

## -description

[TraceLogging wrapper macro](/windows/desktop/tracelogging/tracelogging-wrapper-macros)
that sets the keyword for the event.

## -parameters

### -param eventKeyword [in]

A 64-bit bitmask used to indicate an event's membership in a set of event
categories. This value must be a compile-time constant.

> [!IMPORTANT]
> ProviderId, Level and Keyword are the primary means for filtering
> events. Other kinds of filtering are possible but have much higher overhead.
> Always assign a meaningful non-zero level and keyword to every event.

See [EVENT_DESCRIPTOR](../evntprov/ns-evntprov-event_descriptor.md) for details
about the event keyword.

## -remarks

`TraceLoggingKeyword(eventKeyword)` can be used as a parameter to an invocation
of a [TraceLoggingWrite](./nf-traceloggingprovider-traceloggingwrite.md) macro
to set the event's keyword. Event keyword is a primary means for filtering
events. Always assign a meaningful (non-zero) keyword to every event.

If no **TraceLoggingKeyword** macros are provided to a **TraceLoggingWrite**
call, the event's default keyword is 0. If multiple **TraceLoggingKeyword**
macros are provided, the values are OR'ed together.

The top 16 bits of the keyword (bitmask 0xFFFF000000000000) are defined by
Microsoft. The low 48 bits of the keyword (bitmask 0x0000FFFFFFFFFFFF) are
defined by the event provider. For example, the event provider might define bit
0 (bitmask 0x1) to be the "I/O" category, bit 1 (bitmask 0x2) to be the "UI"
category, and bit 2 (bitmask 0x4) to be the "performance measurement" category.
In this scenario, an event might have its keyword set to 0x5, indicating that
the event is in both the "I/O" and "performance measurement" categories.

## -see-also

[EVENT_DESCRIPTOR](../evntprov/ns-evntprov-event_descriptor.md)

[TraceLoggingWrite](./nf-traceloggingprovider-traceloggingwrite.md)

[TraceLogging wrapper macros](/windows/desktop/tracelogging/tracelogging-wrapper-macros)
