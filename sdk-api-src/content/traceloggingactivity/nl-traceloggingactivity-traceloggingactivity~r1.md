---
UID: NL:traceloggingactivity.TraceLoggingActivity-r1
title: TraceLoggingActivity
description: TBD
helpviewer_keywords: ["- TraceLoggingActivity"]
tech.root: tracelogging
ms.assetid: b5fb71bf-1906-4b9d-a845-b8bd92e8042d
ms.date: 11/14/2019
f1_keywords:
  - traceloggingactivity/TraceLoggingActivity
dev_langs:
  - c++
req.header: traceloggingactivity.h
req.include-header:
req.redist:
req.target-type:
req.target-min-winverclnt:
req.target-min-winversvr:
req.umdf-ver:
req.ddi-compliance:
req.unicode-ansi:
req.idl:
req.max-support:
req.namespace:
req.assembly:
req.type-library:
topic_type:
  - apiref
api_type:
  - COM
api_location:
  - traceloggingactivity.h
api_name:
  - TraceLoggingActivity
targetos: Windows
---

# TraceLoggingActivity class

## -description

Provides support for logging ETW events during an activity. All events must be
manually tagged or nested.

## -remarks

In order to use TraceLogging activities, you need to define an instance of
either **TraceLoggingActivity** or
[TraceLoggingThreadActivity](nl-traceloggingactivity-traceloggingthreadactivity.md).
After you have created an instance of one of these classes, you manipulate
activity logging using
[TraceLoggingFunction](./nf-traceloggingactivity-traceloggingfunction.md),
[TraceLoggingWriteStart](./nf-traceloggingactivity-traceloggingwritestart.md),
[TraceLoggingWriteStop](./nf-traceloggingactivity-traceloggingwritestop.md), and
[TraceLoggingWriteTagged](./nf-traceloggingactivity-traceloggingwritetagged.md).
This class automatically creates a unique identifier when tracing is turned on
and the activity is started.

You can nest activities manually by providing unique identifiers to the
[TraceLoggingWriteStart](./nf-traceloggingactivity-traceloggingwritestart.md)
and [TraceLoggingWriteStop](./nf-traceloggingactivity-traceloggingwritestop.md)
macros.

## -see-also

[TraceLoggingThreadActivity Class](./nl-traceloggingactivity-traceloggingthreadactivity.md)
