---
UID: NC:evntrace.PEVENT_CALLBACK
title: PEVENT_CALLBACK
author: windows-sdk-content
description: Consumers implement this function to receive events from a session. The PEVENT_CALLBACK type defines a pointer to this callback function. EventCallback is a placeholder for the application-defined function name.
old-location: etw\eventcallback.htm
tech.root: etw
ms.assetid: 9312eaed-2997-4d44-952a-fcae3b262947
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: EventCallback, EventCallback callback function [ETW], PEVENT_CALLBACK, PEVENT_CALLBACK callback, _evt_eventcallback, base.eventcallback, etw.eventcallback, evntrace/EventCallback
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - EventCallback
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PEVENT_CALLBACK callback function


## -description


Consumers implement this function to receive events from a session. 

The <b>PEVENT_CALLBACK</b> type defines a pointer to this callback function. <b>EventCallback</b> is a placeholder for the application-defined function name.


## -parameters




### -param pEvent [in]

Pointer to an 
<a href="https://msdn.microsoft.com/d8a6b63e-0cd4-4d19-b0b3-16bb0d33e4c0">EVENT_TRACE</a> structure that contains the event information.


## -returns



The function does not return a value.
					




## -remarks



To specify the function that ETW calls to deliver the events, set the 
<b>EventCallback</b> member of the 
<a href="https://msdn.microsoft.com/179451e9-7e3c-4d3a-bcc6-3ad9d382229a">EVENT_TRACE_LOGFILE</a> structure that you pass to the 
<a href="https://msdn.microsoft.com/505e643b-6b4f-4f93-96c8-7fe8abdd6234">OpenTrace</a> function.

This callback receives all events that the session generates from the time you call the 
<a href="https://msdn.microsoft.com/505e643b-6b4f-4f93-96c8-7fe8abdd6234">OpenTrace</a> function to open the trace. Call the <a href="https://msdn.microsoft.com/aea25a95-f435-4068-9b15-7473f31ebf16">ProcessTrace</a> function to begin receiving the events.

The event data for the first event you always receive contains the <a href="https://msdn.microsoft.com/13fdabe6-c904-4546-b876-c145f6a6c345">TRACE_LOGFILE_HEADER</a> information. 

All the other events you receive contain provider-specific event data. You use the <b>Header.Guid</b> and <b>Header.Class.Type</b> members of <a href="https://msdn.microsoft.com/d8a6b63e-0cd4-4d19-b0b3-16bb0d33e4c0">EVENT_TRACE</a> to determine the type of event you received. If you are consuming events from your own provider and know the layout of the data, this is not an issue. Otherwise, to interpret the event, the provider must have published their event schema in the \\root\wmi namespace. For information on using an event's MOF schema to interpret the event, see <a href="https://msdn.microsoft.com/039a9f66-228e-4258-9967-2b2cd7d31091">Consuming Events</a>.


#### Examples

For an example implementation of an 
<b>EventCallback</b> function, see 
<a href="https://msdn.microsoft.com/13512236-c416-43ba-bf36-b05c5c08d6c9">Retrieving Event Data Using MOF</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/0cfe2f62-63dc-45a6-96ce-fb4bf458358f">BufferCallback</a>



<a href="https://msdn.microsoft.com/179451e9-7e3c-4d3a-bcc6-3ad9d382229a">EVENT_TRACE_LOGFILE</a>



<a href="https://msdn.microsoft.com/32e94f58-b8b6-4e0a-b53b-716a534ac374">EventClassCallback</a>



<a href="https://msdn.microsoft.com/aea25a95-f435-4068-9b15-7473f31ebf16">ProcessTrace</a>
 

 

