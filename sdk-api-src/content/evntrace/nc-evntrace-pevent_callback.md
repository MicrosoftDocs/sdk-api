---
UID: NC:evntrace.PEVENT_CALLBACK
title: PEVENT_CALLBACK (evntrace.h)
description: Consumers implement this function to receive events from a session. The PEVENT_CALLBACK type defines a pointer to this callback function. EventCallback is a placeholder for the application-defined function name.
helpviewer_keywords: ["EventCallback","EventCallback callback function [ETW]","PEVENT_CALLBACK","PEVENT_CALLBACK callback","_evt_eventcallback","base.eventcallback","etw.eventcallback","evntrace/EventCallback"]
old-location: etw\eventcallback.htm
tech.root: ETW
ms.assetid: 9312eaed-2997-4d44-952a-fcae3b262947
ms.date: 12/05/2018
ms.keywords: EventCallback, EventCallback callback function [ETW], PEVENT_CALLBACK, PEVENT_CALLBACK callback, _evt_eventcallback, base.eventcallback, etw.eventcallback, evntrace/EventCallback
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PEVENT_CALLBACK
 - evntrace/PEVENT_CALLBACK
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Evntrace.h
api_name:
 - EventCallback
---

# PEVENT_CALLBACK callback function


## -description

Consumers implement this function to receive events from a session. 

The <b>PEVENT_CALLBACK</b> type defines a pointer to this callback function. <b>EventCallback</b> is a placeholder for the application-defined function name.

## -parameters

### -param pEvent [in]

Pointer to an 
<a href="/windows/desktop/ETW/event-trace">EVENT_TRACE</a> structure that contains the event information.

## -remarks

To specify the function that ETW calls to deliver the events, set the 
<b>EventCallback</b> member of the 
<a href="/windows/desktop/ETW/event-trace-logfile">EVENT_TRACE_LOGFILE</a> structure that you pass to the 
<a href="/windows/desktop/ETW/opentrace">OpenTrace</a> function.

This callback receives all events that the session generates from the time you call the 
<a href="/windows/desktop/ETW/opentrace">OpenTrace</a> function to open the trace. Call the <a href="/windows/desktop/ETW/processtrace">ProcessTrace</a> function to begin receiving the events.

The event data for the first event you always receive contains the <a href="/windows/desktop/ETW/trace-logfile-header">TRACE_LOGFILE_HEADER</a> information. 

All the other events you receive contain provider-specific event data. You use the <b>Header.Guid</b> and <b>Header.Class.Type</b> members of <a href="/windows/desktop/ETW/event-trace">EVENT_TRACE</a> to determine the type of event you received. If you are consuming events from your own provider and know the layout of the data, this is not an issue. Otherwise, to interpret the event, the provider must have published their event schema in the \\root\wmi namespace. For information on using an event's MOF schema to interpret the event, see <a href="/windows/desktop/ETW/consuming-events">Consuming Events</a>.


#### Examples

For an example implementation of an 
<b>EventCallback</b> function, see 
<a href="/windows/desktop/ETW/retrieving-event-data-using-mof">Retrieving Event Data Using MOF</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/ETW/buffercallback">BufferCallback</a>



<a href="/windows/desktop/ETW/event-trace-logfile">EVENT_TRACE_LOGFILE</a>



<a href="/windows/desktop/ETW/eventclasscallback">EventClassCallback</a>



<a href="/windows/desktop/ETW/processtrace">ProcessTrace</a>