---
UID: NS:evntprov._EVENT_FILTER_EVENT_ID
title: "_EVENT_FILTER_EVENT_ID"
author: windows-sdk-content
description: Defines event IDs used in an EVENT_FILTER_DESCRIPTOR structure for an event ID or stack walk filter.
old-location: etw\event_filter_event_id.htm
tech.root: etw
ms.assetid: D660D140-BE86-44F6-B1D2-E1B97300BD11
ms.author: windowssdkdev
ms.date: 10/04/2018
ms.keywords: "*PEVENT_FILTER_EVENT_ID, EVENT_FILTER_EVENT_ID, EVENT_FILTER_EVENT_ID structure [ETW], PEVENT_FILTER_EVENT_ID, PEVENT_FILTER_EVENT_ID structure pointer [ETW], _EVENT_FILTER_EVENT_ID, etw.event_filter_event_id, evntprov/EVENT_FILTER_EVENT_ID, evntprov/PEVENT_FILTER_EVENT_ID"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: evntprov.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
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
 - Evntprov.h
api_name:
 - EVENT_FILTER_EVENT_ID
product: Windows
targetos: Windows
req.typenames: EVENT_FILTER_EVENT_ID, *PEVENT_FILTER_EVENT_ID
req.redist: 
---

# _EVENT_FILTER_EVENT_ID structure


## -description


The <b>EVENT_FILTER_EVENT_ID</b> structure defines event IDs used in an <a href="https://msdn.microsoft.com/9318868a-29d8-4a5e-9579-c06a7c0fd78f">EVENT_FILTER_DESCRIPTOR</a> structure for an  event ID or stack walk filter. 


## -struct-fields




### -field FilterIn

A value that indicates whether filtering should be enabled or disabled for the event IDs passed in the <b>Events</b> member. 

When this member is <b>TRUE</b>, filtering is enabled for the specified event IDs. When this member is <b>FALSE</b>, filtering is disabled for the event IDs. 


### -field Reserved

A reserved value.


### -field Count

The number of event IDs in the <b>Events</b> member.


### -field Events

An array of event IDs.


## -remarks



The <b>EVENT_FILTER_EVENT_ID</b> structure is used in the <a href="https://msdn.microsoft.com/9318868a-29d8-4a5e-9579-c06a7c0fd78f">EVENT_FILTER_DESCRIPTOR</a> structure when the <b>Type</b> member of the <b>EVENT_FILTER_DESCRIPTOR</b> is set to  <b>EVENT_FILTER_TYPE_EVENT_ID</b> or <b>EVENT_FILTER_TYPE_STACKWALK</b>.   This corresponds to an event ID filter (one of the possible scope filters) or a stack walk filter. The <b>EVENT_FILTER_EVENT_ID</b> structure contains an array of event IDs and a Boolean value that indicates if filtering is enabled or disabled for the specified event IDs.




## -see-also




<a href="https://msdn.microsoft.com/bc7cf886-f763-428a-9e75-031e8df26554">ENABLE_TRACE_PARAMETERS</a>



<a href="https://msdn.microsoft.com/9318868a-29d8-4a5e-9579-c06a7c0fd78f">EVENT_FILTER_DESCRIPTOR</a>



<a href="https://msdn.microsoft.com/3aceffb6-614f-4cad-bbec-f181f0cbdbff">EnableTraceEx2</a>
 

 

