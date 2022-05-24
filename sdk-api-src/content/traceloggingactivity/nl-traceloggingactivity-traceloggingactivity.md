---
UID: NL:traceloggingactivity.TraceLoggingActivity
title: TraceLoggingActivity
description:
  Provides support for logging ETW events during an activity. All events must be
  manually tagged or nested.
helpviewer_keywords:
  [
    "TraceLoggingActivity",
    "TraceLoggingActivity class",
    "TraceLoggingActivity class",
    "tracelogging.traceloggingactivity",
    "traceloggingactivity/TraceLoggingActivity",
  ]
old-location: tracelogging\traceloggingactivity.htm
tech.root: tracelogging
ms.assetid: 75930876-4DF2-4559-BA06-133FC676B1AD
ms.date: 12/05/2018
ms.keywords:
  TraceLoggingActivity, TraceLoggingActivity class, TraceLoggingActivity class,
  tracelogging.traceloggingactivity, traceloggingactivity/TraceLoggingActivity
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
f1_keywords:
  - TraceLoggingActivity
  - traceloggingactivity/TraceLoggingActivity
dev_langs:
  - c++
topic_type:
  - APIRef
  - kbSyntax
api_type:
  - COM
api_location:
  - traceloggingactivity.h
api_name:
  - TraceLoggingActivity
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
