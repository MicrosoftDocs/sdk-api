---
UID: NC:evntrace.PEVENT_RECORD_CALLBACK
title: PEVENT_RECORD_CALLBACK (evntrace.h)
description: Consumers implement this callback to receive events from a session. The PEVENT_RECORD_CALLBACK type defines a pointer to this callback function. EventRecordCallback is a placeholder for the application-defined function name.
old-location: etw\eventrecordcallback.htm
tech.root: ETW
ms.assetid: 80a30faf-af1f-4440-8a17-9df44bdb2291
ms.date: 12/05/2018
ms.keywords: EventRecordCallback, EventRecordCallback callback function [ETW], PEVENT_RECORD_CALLBACK, PEVENT_RECORD_CALLBACK callback, etw.eventrecordcallback, evntrace/EventRecordCallback
f1_keywords:
- evntrace/EventRecordCallback
dev_langs:
- c++
req.header: evntrace.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
- EventRecordCallback
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PEVENT_RECORD_CALLBACK callback function


## -description


Consumers implement this callback to receive events from a session. 

The <b>PEVENT_RECORD_CALLBACK</b> type defines a pointer to this callback function. <b>EventRecordCallback</b> is a placeholder for the application-defined function name.


## -parameters




### -param EventRecord [in]

Pointer to an 
<a href="https://docs.microsoft.com/windows/desktop/api/evntcons/ns-evntcons-event_record">EVENT_RECORD</a> structure that contains the event information.


## -returns



The function does not return a value.
					




## -remarks



To specify the function that ETW calls to deliver events, set the 
<b>EventRecordCallback</b> member of the 
<a href="https://docs.microsoft.com/windows/desktop/ETW/event-trace-logfile">EVENT_TRACE_LOGFILE</a> structure (you pass this structure to the 
<a href="https://docs.microsoft.com/windows/desktop/ETW/opentrace">OpenTrace</a> function). You must also set the <b>ProcessTraceMode</b> member to PROCESS_TRACE_MODE_EVENT_RECORD.

This callback receives all events that the session generates from the time you call the 
<a href="https://docs.microsoft.com/windows/desktop/ETW/opentrace">OpenTrace</a> function. Call the <a href="https://docs.microsoft.com/windows/desktop/ETW/processtrace">ProcessTrace</a> function to begin receiving the events.

For information on parsing the event data, see <a href="https://docs.microsoft.com/windows/desktop/ETW/retrieving-event-data-using-tdh">Retrieving Event Data Using TDH</a>. 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/ETW/buffercallback">BufferCallback</a>



<a href="https://docs.microsoft.com/windows/desktop/ETW/event-trace-logfile">EVENT_TRACE_LOGFILE</a>



<a href="https://docs.microsoft.com/windows/desktop/ETW/processtrace">ProcessTrace</a>
 

 

