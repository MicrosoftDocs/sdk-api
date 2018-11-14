---
UID: NF:pla.IAlertDataCollector.put_AlertThresholds
title: IAlertDataCollector::put_AlertThresholds
author: windows-sdk-content
description: Retrieves or sets a list of performance counters and thresholds to monitor.
old-location: pla\ialertdatacollector_alertthresholds.htm
tech.root: PLA
ms.assetid: e0d504ea-58d4-48fd-9baf-851505d6d3ac
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: AlertThresholds property [PLA], AlertThresholds property [PLA],IAlertDataCollector interface, IAlertDataCollector interface [PLA],AlertThresholds property, IAlertDataCollector.AlertThresholds, IAlertDataCollector.put_AlertThresholds, IAlertDataCollector::AlertThresholds, IAlertDataCollector::get_AlertThresholds, IAlertDataCollector::put_AlertThresholds, base.ialertdatacollector_alertthresholds, pla.ialertdatacollector_alertthresholds, pla/IAlertDataCollector::AlertThresholds, pla/IAlertDataCollector::get_AlertThresholds, pla/IAlertDataCollector::put_AlertThresholds, put_AlertThresholds
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: pla.h
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
req.dll: Pla.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Pla.dll
api_name:
 - IAlertDataCollector.AlertThresholds
 - IAlertDataCollector.get_AlertThresholds
 - IAlertDataCollector.put_AlertThresholds
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- pla.h
: 
- IAlertDataCollector.put_AlertThresholds
: 
---

# IAlertDataCollector::put_AlertThresholds


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
 

 

