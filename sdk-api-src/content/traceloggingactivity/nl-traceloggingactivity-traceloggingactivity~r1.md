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

Provides support for logging ETW events during an activity. All events must be manually tagged or nested.




## -remarks

In order to use TraceLogging activities, you need to define an instance of either <b>TraceLoggingActivity</b> or <a href="/windows/desktop/api/traceloggingactivity/nl-traceloggingactivity-traceloggingthreadactivity-r1">TraceLoggingThreadActivity</a>. After you have created an instance of one of these classes, you manipulate activity logging using <a href="/windows/desktop/api/traceloggingactivity/nf-traceloggingactivity-traceloggingfunction">TraceLoggingFunction</a>, <a href="/windows/desktop/api/traceloggingactivity/nf-traceloggingactivity-traceloggingwritestart">TraceLoggingWriteStart</a>, <a href="/windows/desktop/api/traceloggingactivity/nf-traceloggingactivity-traceloggingwritestop">TraceLoggingWriteStop</a>, and <a href="/windows/desktop/api/traceloggingactivity/nf-traceloggingactivity-traceloggingwritetagged">TraceLoggingWriteTagged</a>. This class automatically creates a unique identifier when it is started and tracing is turned on.
         

You can nest activities manually by providing unique identifiers to the <a href="/windows/desktop/api/traceloggingactivity/nf-traceloggingactivity-traceloggingwritestart">TraceLoggingWriteStart</a> and <a href="/windows/desktop/api/traceloggingactivity/nf-traceloggingactivity-traceloggingwritestop">TraceLoggingWriteStop</a> macros.
         



## -see-also


<a href="/windows/desktop/api/traceloggingactivity/nl-traceloggingactivity-traceloggingthreadactivity-r1">TraceLoggingThreadActivity Class</a>
 