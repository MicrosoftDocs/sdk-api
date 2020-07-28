---
UID: NF:traceloggingactivity.TraceLoggingWriteTagged
title: TraceLoggingWriteTagged macro (traceloggingactivity.h)
description: Logs an event with an associated ETW activity id.
helpviewer_keywords: ["TraceLoggingWriteTagged","TraceLoggingWriteTagged macro","tracelogging.traceloggingwritetagged","traceloggingactivity/TraceLoggingWriteTagged"]
old-location: tracelogging\traceloggingwritetagged.htm
tech.root: tracelogging
ms.assetid: BBDFC2B1-33C6-4D5F-AA7B-91BB2A757B1E
ms.date: 12/05/2018
ms.keywords: TraceLoggingWriteTagged, TraceLoggingWriteTagged macro, tracelogging.traceloggingwritetagged, traceloggingactivity/TraceLoggingWriteTagged
f1_keywords:
- traceloggingactivity/TraceLoggingWriteTagged
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- traceloggingactivity.h
api_name:
- TraceLoggingWriteTagged
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# TraceLoggingWriteTagged macro


## -description


Logs an event with an associated ETW activity id.

The activity must have been started, and must not have been stopped yet.


## -parameters




### -param activity [in]

The activity that this method will use to tag the event.


### -param name [in]

The name of the event. This must be a string literal and not a variable. It cannot have any embedded nul characters.


#### - args [in, optional]

Additional parameters added to the event. The maximum number of optional parameters is 99. All parameters must be wrapper macros as defined in <a href="https://docs.microsoft.com/windows/desktop/tracelogging/tracelogging-wrapper-macros">TraceLogging Wrapper Macros</a>.

<b>TraceLoggingWriteTagged</b> does not use the activity’s level or keyword – the default level is 5 (verbose) and the default keyword is 0 (none). Unlike with <b>TraceLoggingWriteStart</b> and <b>TraceLoggingWriteStop</b>, it is ok to use <b>TraceLoggingLevel</b> and <b>TraceLoggingKeyword</b> as args here. 

