---
UID: NF:traceloggingactivity.TraceLoggingWriteStart
title: TraceLoggingWriteStart macro
author: windows-sdk-content
description: Starts an activity and logs the start event.
old-location: tracelogging\traceloggingwritestart.htm
old-project: tracelogging
ms.assetid: E5B9347E-50A7-49BE-BDD5-DCED39371234
ms.author: windowssdkdev
ms.date: 04/26/2018
ms.keywords: TraceLoggingWriteStart, TraceLoggingWriteStart macro, tracelogging.traceloggingwritestart, traceloggingactivity/TraceLoggingWriteStart
ms.prod: windows
ms.technology: windows-sdk
ms.topic: macro
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
tech.root: 
req.typenames: TPMVSCMGR_ERROR
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	traceloggingactivity.h
api_name:
-	TraceLoggingWriteStart
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# TraceLoggingWriteStart macro


## -description


Starts an activity and logs the start event.

The activity must not have already been started.


## -parameters




### -param activity [in]

The activity to start.


### -param name

TBD


#### - EventName [in]

The name of the event. This must be a string literal and not a variable. It cannot have any embedded nul characters.


#### - args [in, optional]

Additional parameters added to the event. The maximum number of optional parameters is 99. All parameters must be wrapper macros as defined in <a href="https://msdn.microsoft.com/806F43F3-D376-4DBD-A4C5-B5F01E5D009D">TraceLogging Wrapper Macros</a>.

The args should not include <b>TraceLoggingLevel</b>, <b>TraceLoggingKeyword</b>, or <b>TraceLoggingOpcode</b>. The level and keyword are set on the activity itself, and the opcode for a start event is always “Start”.


## -see-also




<a href="https://msdn.microsoft.com/638F08E3-5970-40B3-8025-E3D81ECA1D2A">TraceLoggingWriteStop</a>
 

 

