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
 

 

