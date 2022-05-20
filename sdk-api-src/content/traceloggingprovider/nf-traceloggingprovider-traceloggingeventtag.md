---
UID: NF:traceloggingprovider.TraceLoggingEventTag
title: TraceLoggingEventTag macro (traceloggingprovider.h)
description: Wrapper macro for setting the event's tag(s).
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
ms.date: 12/05/2018
ms.keywords:
  TraceLoggingEventTag, TraceLoggingEventTag macro,
  tracelogging.traceloggingeventtag, traceloggingprovider/TraceLoggingEventTag
req.header: traceloggingprovider.h
req.include-header:
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2
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

## -description

Wrapper macro for setting the event's tag(s).

## -parameters

### -param eventTag [in]

A compile-time constant in the range of 0x00200000-0x0FE00000.

## -remarks

The semantics of the tags are defined by the event consumer. During event
processing, this tag can be retrieved from the
[TRACE_EVENT_INFO](../tdh/ns-tdh-trace_event_info.md) Tags field.

The TraceLogging schema convention encodes tags as 28-bit fields by using a
chain of up to four bytes with the upper-most bit used as a 'chain' bit (4\*7 =
28). Data is encoded most-significant byte first.
[TraceLoggingWrite](./nf-traceloggingprovider-traceloggingwrite.md) and
TraceLoggingEventTag only supports encoding a single byte of tag data, which
must then contain the upper-most range of seven bits, thus 0x0FE00000.

If no parameters are provided, no tag is transmitted for the event. If multiple
args are provided, they are OR'ed together.
