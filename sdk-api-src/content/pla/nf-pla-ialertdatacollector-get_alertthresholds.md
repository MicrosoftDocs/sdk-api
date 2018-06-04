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

# IAlertDataCollector::get_AlertThresholds


## -description


Retrieves or sets a list of performance counters and thresholds to monitor. 

This property is read/write.


## -parameters


## -remarks



You must specify at least one alert threshold. If the counter value crosses the specified threshold value, PLA performs one or more of the following actions:

<ul>
<li>Logs event 2031 to the  Microsoft-Windows-Diagnosis-PLA/Operational event log if the <a href="https://msdn.microsoft.com/3ba20fac-5817-47ed-a934-e43f49f0a121">IAlertDataCollector::EventLog</a>  property is true.</li>
<li>Starts the task in the <a href="https://msdn.microsoft.com/a86f8524-3564-4a65-9574-1709f82280d8">IAlertDataCollector::Task</a>  property, if specified.</li>
<li>Triggers the data collector set specified in the <a href="https://msdn.microsoft.com/3ba9b1c0-432e-4caf-a082-33d1c5c3b132">IAlertDataCollector::TriggerDataCollectorSet</a>  property to run, if specified.</li>
</ul>
If you use XML to define the alert, you must use "&amp;gt;" for the greater than sign (&gt;) and "&amp;lt;" for the less than sign (&lt;).




## -see-also




<a href="https://msdn.microsoft.com/61907979-fa4a-45da-96c5-7cd12021fbb7">IAlertDataCollector</a>
 

 

