---
UID: NC:evntrace.PEVENT_TRACE_BUFFER_CALLBACKW
title: PEVENT_TRACE_BUFFER_CALLBACKW (evntrace.h)
author: windows-sdk-content
description: Consumers implement this function to receive statistics about each buffer of events that ETW delivers to an event trace consumer.
old-location: etw\buffercallback.htm
tech.root: ETW
ms.assetid: 0cfe2f62-63dc-45a6-96ce-fb4bf458358f
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: BufferCallback, BufferCallback callback function [ETW], PEVENT_TRACE_BUFFER_CALLBACK, PEVENT_TRACE_BUFFER_CALLBACK callback, PEVENT_TRACE_BUFFER_CALLBACKA, PEVENT_TRACE_BUFFER_CALLBACKW, _evt_buffercallback, base.buffercallback, etw.buffercallback, evntrace/BufferCallback
ms.topic: callback
req.header: evntrace.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - UserDefined
api_location:
 - Evntrace.h
api_name:
 - BufferCallback
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PEVENT_TRACE_BUFFER_CALLBACKW callback function


## -description


Consumers implement this function to  receive statistics about each buffer of events that ETW delivers to an event trace consumer. ETW calls this function after the events for each buffer are delivered.
			

The <b>PEVENT_TRACE_BUFFER_CALLBACK</b> type defines a pointer to this callback function. <b>BufferCallback</b> is a placeholder for the application-defined function name.


## -parameters




### -param Logfile








#### - Buffer [in]

Pointer to an 
<a href="https://msdn.microsoft.com/179451e9-7e3c-4d3a-bcc6-3ad9d382229a">EVENT_TRACE_LOGFILE</a> structure that contains information about the buffer. 


## -returns



To continue processing events, return <b>TRUE</b>. Otherwise, return <b>FALSE</b>.
					Returning <b>FALSE</b> will terminate the <a href="https://msdn.microsoft.com/aea25a95-f435-4068-9b15-7473f31ebf16">ProcessTrace</a> function.




## -remarks



To specify the function that ETW calls to deliver the buffer statistics, set the 
<b>BufferCallback</b> member of the 
<a href="https://msdn.microsoft.com/179451e9-7e3c-4d3a-bcc6-3ad9d382229a">EVENT_TRACE_LOGFILE</a> structure that you pass to the 
<a href="https://msdn.microsoft.com/505e643b-6b4f-4f93-96c8-7fe8abdd6234">OpenTrace</a> function.


#### Examples

For an example implementation of a 
<b>BufferCallback</b> function, see 
<a href="https://msdn.microsoft.com/13512236-c416-43ba-bf36-b05c5c08d6c9">Retrieving Event Data Using MOF</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/179451e9-7e3c-4d3a-bcc6-3ad9d382229a">EVENT_TRACE_LOGFILE</a>



<a href="https://msdn.microsoft.com/aea25a95-f435-4068-9b15-7473f31ebf16">ProcessTrace</a>
 

 

