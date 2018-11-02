---
UID: NF:traceloggingprovider.TraceLoggingWriteActivity
title: TraceLoggingWriteActivity macro
author: windows-sdk-content
description: Emits an event with specific activity IDs.
old-location: tracelogging\traceloggingwriteactivity.htm
tech.root: tracelogging
ms.assetid: 1BFEC534-A9D4-4310-9E40-FCC1AB301D0F
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: TraceLoggingWriteActivity, TraceLoggingWriteActivity macro, tracelogging.traceloggingwriteactivity, traceloggingprovider/TraceLoggingWriteActivity
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - traceloggingprovider.h
api_name:
 - TraceLoggingWriteActivity
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# TraceLoggingWriteActivity macro


## -description


Emits an event with specific activity IDs.


## -parameters




### -param hProvider [in]

A provider registration handle.


### -param eventName [in]

The name of the event. This must be a string literal and not a variable. It cannot have any embedded nul characters.


### -param pActivityId [in, optional]

The activity id for the event.


### -param pRelatedActivityId [in, optional]

The related activity id for the event.


#### - args [in, optional]

Additional parameters added to the event. The maximum number of optional parameters is 99. All parameters must be wrapper macros as defined in <a href="https://msdn.microsoft.com/806F43F3-D376-4DBD-A4C5-B5F01E5D009D">TraceLogging Wrapper Macros</a>.


## -remarks



This macro functions the same as <a href="https://msdn.microsoft.com/BFBC6802-64DC-478E-B09D-F550135994AB">TraceLoggingWrite</a> except for the addition of the activity ids. If you submit <b>NULL</b> for the activity ids, this macro will be identical to TraceLoggingWrite.
     

When submitting the optional parameters, you might generate an error that a line is too long or the compiler is out of heap space. This may occur because a line of code is longer than the maximum length allowed by the compiler. In this case, the parameters are too complex and you need to remove some from the macro to get it to work. 
     

The maximum number of event data descriptors is 128. Since each parameter can have 0, 1, or 2, it is possible to hit the data descriptor limit before the argument limit. In addition, the maximum number of bytes per event is 65536.
     



