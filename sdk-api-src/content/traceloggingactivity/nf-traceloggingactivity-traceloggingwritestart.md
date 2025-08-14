---
UID: NF:traceloggingactivity.TraceLoggingWriteStart
title: TraceLoggingWriteStart macro (traceloggingactivity.h)
description: Starts an activity and logs the start event.
helpviewer_keywords:
  [
    "TraceLoggingWriteStart",
    "TraceLoggingWriteStart macro",
    "tracelogging.traceloggingwritestart",
    "traceloggingactivity/TraceLoggingWriteStart",
  ]
old-location: tracelogging\traceloggingwritestart.htm
tech.root: tracelogging
ms.assetid: E5B9347E-50A7-49BE-BDD5-DCED39371234
ms.date: 07/01/2025
ms.keywords:
  TraceLoggingWriteStart, TraceLoggingWriteStart macro,
  tracelogging.traceloggingwritestart,
  traceloggingactivity/TraceLoggingWriteStart
req.header: traceloggingactivity.h
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
  - TraceLoggingWriteStart
  - traceloggingactivity/TraceLoggingWriteStart
dev_langs:
  - c++
topic_type:
  - APIRef
  - kbSyntax
api_type:
  - HeaderDef
api_location:
  - traceloggingactivity.h
api_name:
  - TraceLoggingWriteStart
---

# TraceLoggingWriteStart macro

## -syntax

```cpp
void TraceLoggingWriteStart(
  [in]            TraceLoggingActivity activity,
  [in]            String name,
  [in, optional]   args
);
```

## -description

Starts an activity and logs the start event.

The activity must not have already been started.

## -parameters

### -param activity [in]

The activity to start.

### -param name [in]

The name of the event. This must be a string literal and not a variable. It
cannot have any embedded nul characters.

#### - args [in, optional]

Additional parameters added to the event. The maximum number of optional
parameters is 99. All parameters must be wrapper macros as defined in
[TraceLogging Wrapper Macros](/windows/win32/tracelogging/tracelogging-wrapper-macros).

The args should not include **TraceLoggingLevel**, **TraceLoggingKeyword**, or
**TraceLoggingOpcode**. The level and keyword are set on the activity itself,
and the opcode for a start event is always "Start".

## -see-also

[TraceLoggingWriteStop](./nf-traceloggingactivity-traceloggingwritestop.md)
