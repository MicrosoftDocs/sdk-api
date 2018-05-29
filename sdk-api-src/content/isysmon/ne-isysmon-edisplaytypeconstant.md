---
UID: NE:isysmon.eDisplayTypeConstant
title: eDisplayTypeConstant
author: windows-sdk-content
description: Determines how the performance counter data is graphed, for example, as a line graph or a histogram.
old-location: sysmon\displaytypeconstants.htm
old-project: SysMon
ms.assetid: c0f991cc-c547-4d4c-ae8f-9f672e11f010
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: DisplayTypeConstants, DisplayTypeConstants enumeration [SysMon], base.displaytypeconstants, eDisplayTypeConstant, isysmon/DisplayTypeConstants, isysmon/sysmonChartArea, isysmon/sysmonChartStackedArea, isysmon/sysmonHistogram, isysmon/sysmonLineGraph, isysmon/sysmonReport, sysmon.displaytypeconstants, sysmonChartArea, sysmonChartStackedArea, sysmonHistogram, sysmonLineGraph, sysmonReport
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: isysmon.h
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
req.typenames: DisplayTypeConstants
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	ISysmon.h
api_name:
-	DisplayTypeConstants
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
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
 

 

