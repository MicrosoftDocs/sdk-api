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

# TraceLoggingChannel macro


## -description


Wrapper macro for setting the event's channel.


## -parameters




### -param eventChannel [in]

The event channel to be logged.


## -remarks



Channels are used in advanced Event Tracing for Windows (ETW) scenarios such as writing to system-defined  event consumers such as the event log. When using channels, a manifest must be  registered with the system to define the provider and its channels. A manifest  for a TraceLogging provider should define the provider and the channels but  should omit the event definitions, since they are managed by TraceLogging.  

The eventChannel parameter must be a compile-time constant 0 to 255. If no  TraceLoggingChannel(n) arg is provided, the default channel level is 11  (WINEVENT_CHANNEL_TRACELOGGING), indicating that this is a normal  TraceLogging event. If multiple TraceLoggingChannel(n) args are provided, the  value from the last TraceLoggingChannel(n) is used.

<div class="alert"><b>Warning</b>  If your provider will run on Windows earlier than Windows 10, do not use  TraceLoggingChannel. For an event to be recognized as TraceLogging-compatible,  it must either have the channel set to 11 or it must have been marked by the  ETW runtime during EventWrite. The Windows 10 ETW runtime will recognize and  mark TraceLogging events regardless of channel, but earlier versions of  Windows require a system update in order to support marking TraceLogging  events. For events captured on systems without an update, the channel is the  only way to recognize a TraceLogging event, so events with other channels may  be harder to decode.  </div>
<div> </div>


