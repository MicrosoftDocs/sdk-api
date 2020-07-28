---
UID: NS:evntrace._EVENT_TRACE
title: EVENT_TRACE (evntrace.h)
description: The EVENT_TRACE structure is used to deliver event information to an event trace consumer.
helpviewer_keywords: ["*PEVENT_TRACE","EVENT_TRACE","EVENT_TRACE structure [ETW]","PEVENT_TRACE","PEVENT_TRACE structure pointer [ETW]","_EVENT_TRACE","_evt_event_trace","base.event_trace","etw.event_trace","evntrace/EVENT_TRACE","evntrace/PEVENT_TRACE"]
old-location: etw\event_trace.htm
tech.root: ETW
ms.assetid: d8a6b63e-0cd4-4d19-b0b3-16bb0d33e4c0
ms.date: 12/05/2018
ms.keywords: '*PEVENT_TRACE, EVENT_TRACE, EVENT_TRACE structure [ETW], PEVENT_TRACE, PEVENT_TRACE structure pointer [ETW], _EVENT_TRACE, _evt_event_trace, base.event_trace, etw.event_trace, evntrace/EVENT_TRACE, evntrace/PEVENT_TRACE'
f1_keywords:
- evntrace/EVENT_TRACE
dev_langs:
- c++
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
- HeaderDef
api_location:
- Evntrace.h
api_name:
- EVENT_TRACE
targetos: Windows
req.typenames: EVENT_TRACE, *PEVENT_TRACE
req.redist: 
ms.custom: 19H1
---

# EVENT_TRACE structure


## -description


The 
<b>EVENT_TRACE</b> structure is used to deliver event information to an event trace consumer.
			
			
		


## -struct-fields




### -field Header

An 
<a href="https://docs.microsoft.com/windows/desktop/ETW/event-trace-header">EVENT_TRACE_HEADER</a> structure that contains standard event tracing information.


### -field InstanceId

Instance identifier. Contains valid data when the 
provider calls the <a href="https://docs.microsoft.com/windows/desktop/ETW/traceeventinstance">TraceEventInstance</a> function to generate the event. Otherwise, the value is zero.


### -field ParentInstanceId

Instance identifier for a parent event. Contains valid data when the 
provider calls the <a href="https://docs.microsoft.com/windows/desktop/ETW/traceeventinstance">TraceEventInstance</a> function to generate the event. Otherwise, the value is zero.


### -field ParentGuid

Class GUID of the parent event. Contains valid data when the 
provider calls the <a href="https://docs.microsoft.com/windows/desktop/ETW/traceeventinstance">TraceEventInstance</a> function to generate the event. Otherwise, the value is zero.


### -field MofData

Pointer to the beginning of the event-specific data for this event.


### -field MofLength

Number of bytes to which <b>MofData</b> points.


### -field DUMMYUNIONNAME

 


### -field DUMMYUNIONNAME.ClientContext

Reserved.


### -field DUMMYUNIONNAME.BufferContext

Provides information about the event such as the session identifier and processor number of the CPU on which the provider process ran. For details, see the <a href="https://docs.microsoft.com/windows/desktop/api/relogger/ns-relogger-etw_buffer_context">ETW_BUFFER_CONTEXT</a> structure.

<b>Prior to Windows Vista:  </b>Not supported.


## -remarks



ETW passes this structure to the 
consumer's <a href="https://docs.microsoft.com/windows/desktop/ETW/eventcallback">EventCallback</a> callback function.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/ETW/eventcallback">EventCallback</a>



<a href="https://docs.microsoft.com/windows/desktop/ETW/eventclasscallback">EventClassCallback</a>
 

 

