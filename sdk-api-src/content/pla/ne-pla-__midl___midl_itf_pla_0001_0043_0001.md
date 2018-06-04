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

# __MIDL___MIDL_itf_pla_0001_0043_0001 enumeration


## -description


Defines the data collector types.


## -enum-fields




### -field plaPerformanceCounter

Collects performance counter data. The <a href="https://msdn.microsoft.com/c9a5f417-ffd5-452d-9218-3ac045a55de0">IPerformanceCounterDataCollector</a> interface represents this data collector.


### -field plaTrace

Collects events from an event trace session. The <a href="https://msdn.microsoft.com/1f57aa92-81f0-445f-baa3-274714e8291e">ITraceDataCollector</a> interface represents this data collector.


### -field plaConfiguration

Collects computer configuration information. The <a href="https://msdn.microsoft.com/7266c02d-0f56-4754-8a67-68394a5f0158">IConfigurationDataCollector</a> interface represents this data collector.


### -field plaAlert

Monitors performance counters and performs actions if the counter value crosses the specified threshold. The <a href="https://msdn.microsoft.com/61907979-fa4a-45da-96c5-7cd12021fbb7">IAlertDataCollector</a> interface represents this data collector.


### -field plaApiTrace

Logs API calls made by the process. The <a href="https://msdn.microsoft.com/8d600d35-bd2b-44fc-9da4-3c6e50e90b65">IApiTracingDataCollector</a> interface represents this data collector.


## -see-also




<a href="https://msdn.microsoft.com/a5ec0e60-555c-4a95-b13d-a22cc8db7c28">IDataCollector::DataCollectorType</a>
 

 

