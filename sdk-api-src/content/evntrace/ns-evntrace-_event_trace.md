---
UID: NS:evntrace._EVENT_TRACE
title: "_EVENT_TRACE"
author: windows-sdk-content
description: The EVENT_TRACE structure is used to deliver event information to an event trace consumer.
old-location: etw\event_trace.htm
old-project: etw
ms.assetid: d8a6b63e-0cd4-4d19-b0b3-16bb0d33e4c0
ms.author: windowssdkdev
ms.date: 08/08/2018
ms.keywords: "*PEVENT_TRACE, EVENT_TRACE, EVENT_TRACE structure [ETW], PEVENT_TRACE, PEVENT_TRACE structure pointer [ETW], _EVENT_TRACE, _evt_event_trace, base.event_trace, etw.event_trace, evntrace/EVENT_TRACE, evntrace/PEVENT_TRACE"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: evntrace.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: EVENT_TRACE, *PEVENT_TRACE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Evntrace.h
api_name:
 - EVENT_TRACE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _EVENT_TRACE structure


## -description


The 
<b>EVENT_TRACE</b> structure is used to deliver event information to an event trace consumer.
			
			
		


## -struct-fields




### -field Header

An 
<a href="https://msdn.microsoft.com/33c2de6b-afc2-4323-8d81-2970e66edf5e">EVENT_TRACE_HEADER</a> structure that contains standard event tracing information.


### -field InstanceId

Instance identifier. Contains valid data when the 
provider calls the <a href="https://msdn.microsoft.com/e8361bdc-21dd-47a0-bdbf-56f4d6195689">TraceEventInstance</a> function to generate the event. Otherwise, the value is zero.


### -field ParentInstanceId

Instance identifier for a parent event. Contains valid data when the 
provider calls the <a href="https://msdn.microsoft.com/e8361bdc-21dd-47a0-bdbf-56f4d6195689">TraceEventInstance</a> function to generate the event. Otherwise, the value is zero.


### -field ParentGuid

Class GUID of the parent event. Contains valid data when the 
provider calls the <a href="https://msdn.microsoft.com/e8361bdc-21dd-47a0-bdbf-56f4d6195689">TraceEventInstance</a> function to generate the event. Otherwise, the value is zero.


### -field MofData

Pointer to the beginning of the event-specific data for this event.


### -field MofLength

Number of bytes to which <b>MofData</b> points.


### -field DUMMYUNIONNAME

 


### -field DUMMYUNIONNAME.ClientContext

Reserved.


### -field DUMMYUNIONNAME.BufferContext

Provides information about the event such as the session identifier and processor number of the CPU on which the provider process ran. For details, see the <a href="https://msdn.microsoft.com/75577305-fb3f-40a2-8fe6-9cd82c3f4e69">ETW_BUFFER_CONTEXT</a> structure.

<b>Prior to Windows Vista:  </b>Not supported.


## -remarks



ETW passes this structure to the 
consumer's <a href="https://msdn.microsoft.com/9312eaed-2997-4d44-952a-fcae3b262947">EventCallback</a> callback function.




## -see-also




<a href="https://msdn.microsoft.com/9312eaed-2997-4d44-952a-fcae3b262947">EventCallback</a>



<a href="https://msdn.microsoft.com/32e94f58-b8b6-4e0a-b53b-716a534ac374">EventClassCallback</a>
 

 

