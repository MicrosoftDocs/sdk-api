---
UID: NF:traceloggingprovider.TraceLoggingWriteActivity
title: TraceLoggingWriteActivity macro (traceloggingprovider.h)
description: Emits an event with specific activity IDs.
helpviewer_keywords:
  [
    "TraceLoggingWriteActivity",
    "TraceLoggingWriteActivity macro",
    "tracelogging.traceloggingwriteactivity",
    "traceloggingprovider/TraceLoggingWriteActivity",
  ]
old-location: tracelogging\traceloggingwriteactivity.htm
tech.root: tracelogging
ms.assetid: 1BFEC534-A9D4-4310-9E40-FCC1AB301D0F
ms.date: 12/05/2018
ms.keywords:
  TraceLoggingWriteActivity, TraceLoggingWriteActivity macro,
  tracelogging.traceloggingwriteactivity,
  traceloggingprovider/TraceLoggingWriteActivity
req.header: traceloggingprovider.h
req.include-header:
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
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
  - TraceLoggingWriteActivity
  - traceloggingprovider/TraceLoggingWriteActivity
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
  - TraceLoggingWriteActivity
---

# TraceLoggingWriteActivity macro

## -description

Emits an event with specific activity IDs.

## -parameters

### -param hProvider [in]

A provider registration handle.

### -param eventName [in]

The name of the event. This must be a string literal and not a variable. It
cannot have any embedded nul characters.

### -param pActivityId [in, optional]

The activity id for the event.

### -param pRelatedActivityId [in, optional]

The related activity id for the event.

#### - args [in, optional]

Additional parameters added to the event. The maximum number of optional
parameters is 99. All parameters must be wrapper macros as defined in
[TraceLogging Wrapper Macros](/windows/desktop/tracelogging/tracelogging-wrapper-macros).

## -remarks

This macro functions the same as
[TraceLoggingWrite](./nf-traceloggingprovider-traceloggingwrite.md) except for
the addition of the activity ids. If you submit **NULL** for the activity ids,
this macro will be identical to TraceLoggingWrite.

When submitting the optional parameters, you might generate an error that a line
is too long or the compiler is out of heap space. This may occur because a line
of code is longer than the maximum length allowed by the compiler. In this case,
the parameters are too complex and you need to remove some from the macro to get
it to work.

The maximum number of event data descriptors is 128. Since each parameter can
have 0, 1, or 2, it is possible to hit the data descriptor limit before the
argument limit. In addition, the maximum number of bytes per event is 65536.
