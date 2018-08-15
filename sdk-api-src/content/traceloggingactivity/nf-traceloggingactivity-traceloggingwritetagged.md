---
UID: NF:traceloggingactivity.TraceLoggingWriteTagged
title: TraceLoggingWriteTagged macro
author: windows-sdk-content
description: Logs an event with an associated ETW activity id.
old-location: tracelogging\traceloggingwritetagged.htm
old-project: tracelogging
ms.assetid: BBDFC2B1-33C6-4D5F-AA7B-91BB2A757B1E
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: TraceLoggingWriteTagged, TraceLoggingWriteTagged macro, tracelogging.traceloggingwritetagged, traceloggingactivity/TraceLoggingWriteTagged
ms.prod: windows
ms.technology: windows-sdk
ms.topic: macro
req.header: traceloggingactivity.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: TPMVSCMGR_ERROR
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - traceloggingactivity.h
api_name:
 - TraceLoggingWriteTagged
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
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

Additional parameters added to the event. The maximum number of optional parameters is 99. All parameters must be wrapper macros as defined in <a href="https://msdn.microsoft.com/806F43F3-D376-4DBD-A4C5-B5F01E5D009D">TraceLogging Wrapper Macros</a>.

<b>TraceLoggingWriteTagged</b> does not use the activity’s level or keyword – the default level is 5 (verbose) and the default keyword is 0 (none). Unlike with <b>TraceLoggingWriteStart</b> and <b>TraceLoggingWriteStop</b>, it is ok to use <b>TraceLoggingLevel</b> and <b>TraceLoggingKeyword</b> as args here. 

