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

# eDisplayTypeConstant enumeration


## -description


Determines how the performance counter data is graphed, for example, as a line graph or a histogram.


## -enum-fields




### -field sysmonLineGraph

Counter values are displayed in a line graph. Each marker on the line graph represents a data value.


### -field sysmonHistogram

Counter values are displayed as a histogram. 


### -field sysmonReport

Counter values are displayed in a report format. Only the current value for each counter is displayed.


### -field sysmonChartArea

Counter values are displayed as a line graph. The area between the line and the x-axis is shaded. You can only use this option if the source of the counter data is a log file.


### -field sysmonChartStackedArea

Counter values are displayed as a line graph. The line graph for each counter is stacked one upon the other. The area between the line and the x-axis or adjacent counter is shaded. You can only use this option if the source of the counter data is a log file.

If the sum of all the counter values exceeds the maximum scale value of the graph, SYSMON uses an appropriate scale value for each counter in order to fit the counters within the maximum scale value of the graph.


## -remarks



The following enumeration values were introduced in Windows Vista.

<ul>
<li><b>sysmonChartArea</b></li>
<li><b>sysmonChartStackedArea</b></li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/a04545b1-920e-4fb3-909b-dc47e1374629">SystemMonitor.DisplayType</a>
 

 

