---
UID: NL:traceloggingactivity.TraceLoggingActivity
title: TraceLoggingActivity
description: Provides support for logging ETW events during an activity. All events must be manually tagged or nested.
helpviewer_keywords: ["TraceLoggingActivity","TraceLoggingActivity class","TraceLoggingActivity class","described","tracelogging.traceloggingactivity","traceloggingactivity/TraceLoggingActivity"]
old-location: tracelogging\traceloggingactivity.htm
tech.root: tracelogging
ms.assetid: 75930876-4DF2-4559-BA06-133FC676B1AD
ms.date: 12/05/2018
ms.keywords: TraceLoggingActivity, TraceLoggingActivity class, TraceLoggingActivity class,described, tracelogging.traceloggingactivity, traceloggingactivity/TraceLoggingActivity
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

Provides support for logging ETW events during an activity. All events must be manually tagged or nested.


## -remarks

In order to use TraceLogging activities, you need to define an instance of either [TraceLoggingThreadActivity](./nl-traceloggingactivity-traceloggingthreadactivity.md). After you have created an instance of one of these classes, you manipulate activity logging using <a href="/windows/desktop/api/traceloggingactivity/nf-traceloggingactivity-traceloggingfunction">TraceLoggingFunction</a>, <a href="/windows/desktop/api/traceloggingactivity/nf-traceloggingactivity-traceloggingwritestart">TraceLoggingWriteStart</a>, <a href="/windows/desktop/api/traceloggingactivity/nf-traceloggingactivity-traceloggingwritestop">TraceLoggingWriteStop</a>, and <a href="/windows/desktop/api/traceloggingactivity/nf-traceloggingactivity-traceloggingwritetagged">TraceLoggingWriteTagged</a>. This class automatically creates a unique identifier when it is started and tracing is turned on.
         

You can nest activities manually by providing unique identifiers to the <a href="/windows/desktop/api/traceloggingactivity/nf-traceloggingactivity-traceloggingwritestart">TraceLoggingWriteStart</a> and <a href="/windows/desktop/api/traceloggingactivity/nf-traceloggingactivity-traceloggingwritestop">TraceLoggingWriteStop</a> macros.

## -see-also

[TraceLoggingThreadActivity](./nl-traceloggingactivity-traceloggingthreadactivity.md)
