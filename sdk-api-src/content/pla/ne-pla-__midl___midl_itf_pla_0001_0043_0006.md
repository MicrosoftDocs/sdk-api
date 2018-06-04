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

# __MIDL___MIDL_itf_pla_0001_0043_0006 enumeration


## -description


Defines where the trace events are delivered.


## -enum-fields




### -field plaFile

Write the trace events to a log file.


### -field plaRealTime

Deliver the trace events to a real time consumer.


### -field plaBoth

Write the trace events to a log file and deliver them to a real-time consumer.


### -field plaBuffering

For details, see the <a href="https://msdn.microsoft.com/d12aaecb-776a-4476-9ba4-16af30fde9c2">EVENT_TRACE_BUFFERING_MODE</a> logging mode in Event Tracing for Windows.


## -see-also




<a href="https://msdn.microsoft.com/eeca98e2-8da1-44e5-8d43-00b52f51bcae">ITraceDataCollector::StreamMode</a>
 

 

