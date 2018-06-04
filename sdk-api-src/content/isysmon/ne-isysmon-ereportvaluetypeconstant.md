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

# eReportValueTypeConstant enumeration


## -description


Determines if the Histogram and Report views graph the last value sampled or a calculated value using values from the sampling period, such as the average or minimum value.


## -enum-fields




### -field sysmonDefaultValue

The value displayed depends on the source of the counter data. If the source of the counter data is from the current activity of the computer, <b>sysmonCurrentValue</b> is used. If the source of the counter data is a log file, <b>sysmonAverage</b> is used.


### -field sysmonCurrentValue

The current value of the counter.


### -field sysmonAverage

The average value of the counter over the sampling period.


### -field sysmonMinimum

The minimum value of the counter over the sampling period.


### -field sysmonMaximum

The maximum value of the counter over the sampling period.


## -see-also




<a href="https://msdn.microsoft.com/add75744-c3ab-48ab-b567-28a072facfdd">SystemMonitor.ReportValueType</a>
 

 

