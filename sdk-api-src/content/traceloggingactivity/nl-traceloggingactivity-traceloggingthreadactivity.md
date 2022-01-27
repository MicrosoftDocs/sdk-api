---
UID: NL:traceloggingactivity.TraceLoggingThreadActivity
title: TraceLoggingThreadActivity (traceloggingactivity.h)
description: Provides support for logging ETW events during an activity. Events will be automatically tagged with or nested in this activity.
helpviewer_keywords: ["TraceLoggingThreadActivity","TraceLoggingThreadActivity class","TraceLoggingThreadActivity class","described","tracelogging.traceloggingthreadactivity","traceloggingactivity/TraceLoggingThreadActivity"]
old-location: tracelogging\traceloggingthreadactivity.htm
tech.root: tracelogging
ms.assetid: 7666A28B-42B2-473F-852F-BD3F6CAA6AC7
ms.date: 12/05/2018
ms.keywords: TraceLoggingThreadActivity, TraceLoggingThreadActivity class, TraceLoggingThreadActivity class,described, tracelogging.traceloggingthreadactivity, traceloggingactivity/TraceLoggingThreadActivity
req.header: traceloggingactivity.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
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
 - TraceLoggingThreadActivity
 - traceloggingactivity/TraceLoggingThreadActivity
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
 - TraceLoggingThreadActivity
---

# TraceLoggingThreadActivity class

## -description

Provides support for logging ETW events during an activity. Events will be automatically tagged with or nested in this activity.


## -remarks

This class works by setting a per-thread variable. Only events occurring on the active thread will be automatically tagged.

In order to use TraceLogging activities, you need to define an instance of either <a href="/windows/desktop/api/traceloggingactivity/nl-traceloggingactivity-traceloggingactivity-r1">TraceLoggingActivity</a> or <b>TraceLoggingThreadActivity</b>. After you have created an instance of one of these classes, you manipulate activity logging using <a href="/windows/desktop/api/traceloggingactivity/nf-traceloggingactivity-traceloggingfunction">TraceLoggingFunction</a>, <a href="/windows/desktop/api/traceloggingactivity/nf-traceloggingactivity-traceloggingwritestart">TraceLoggingWriteStart</a>, <a href="/windows/desktop/api/traceloggingactivity/nf-traceloggingactivity-traceloggingwritestop">TraceLoggingWriteStop</a>, and <a href="/windows/desktop/api/traceloggingactivity/nf-traceloggingactivity-traceloggingwritetagged">TraceLoggingWriteTagged</a>. This class automatically creates a unique identifier when it is started and tracing is turned on.
         

Any active threads will be automatically nested in this instance when you start logging with a <b>TraceLoggingThreadActivity</b> object. In addition, all events will be automatically logged with this object's unique identifier.
         

<div class="alert"><b>Caution</b>  <p class="note">Only use this class when you can guarantee that all activities for this thread are fully nested. You must ensure that no child activity will outlast a parent activity, even in error cases or edge cases.
           

<p class="note">In DEBUG builds, the class will raise an assertion during its Stop event, if it detects incorrect activity nesting, or if the Stop event occurs on a thread other than the thread used to start it.

</div>
<div> </div>
This class is not available for store applications.

## -see-also

<a href="/windows/desktop/api/traceloggingactivity/nl-traceloggingactivity-traceloggingactivity-r1">TraceLoggingActivity Class</a>
