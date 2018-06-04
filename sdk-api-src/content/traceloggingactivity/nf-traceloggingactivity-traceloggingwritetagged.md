---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# TraceLoggingWriteTagged macro


## -description


Logs an event with an associated ETW activity id.

The activity must have been started, and must not have been stopped yet.


## -parameters




### -param activity [in]

The activity that this method will use to tag the event.


### -param name

TBD


#### - EventName [in]

The name of the event. This must be a string literal and not a variable. It cannot have any embedded nul characters.


#### - args [in, optional]

Additional parameters added to the event. The maximum number of optional parameters is 99. All parameters must be wrapper macros as defined in <a href="https://msdn.microsoft.com/806F43F3-D376-4DBD-A4C5-B5F01E5D009D">TraceLogging Wrapper Macros</a>.

<b>TraceLoggingWriteTagged</b> does not use the activity’s level or keyword – the default level is 5 (verbose) and the default keyword is 0 (none). Unlike with <b>TraceLoggingWriteStart</b> and <b>TraceLoggingWriteStop</b>, it is ok to use <b>TraceLoggingLevel</b> and <b>TraceLoggingKeyword</b> as args here. 

