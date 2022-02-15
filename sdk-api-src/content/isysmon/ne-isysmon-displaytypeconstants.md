---
UID: NE:isysmon.eDisplayTypeConstant
title: DisplayTypeConstants (isysmon.h)
description: Determines how the performance counter data is graphed, for example, as a line graph or a histogram.
helpviewer_keywords: ["DisplayTypeConstants","DisplayTypeConstants enumeration [SysMon]","base.displaytypeconstants","isysmon/DisplayTypeConstants","isysmon/sysmonChartArea","isysmon/sysmonChartStackedArea","isysmon/sysmonHistogram","isysmon/sysmonLineGraph","isysmon/sysmonReport","sysmon.displaytypeconstants","sysmonChartArea","sysmonChartStackedArea","sysmonHistogram","sysmonLineGraph","sysmonReport"]
old-location: sysmon\displaytypeconstants.htm
tech.root: SysMon
ms.assetid: c0f991cc-c547-4d4c-ae8f-9f672e11f010
ms.date: 12/05/2018
ms.keywords: DisplayTypeConstants, DisplayTypeConstants enumeration [SysMon], base.displaytypeconstants, isysmon/DisplayTypeConstants, isysmon/sysmonChartArea, isysmon/sysmonChartStackedArea, isysmon/sysmonHistogram, isysmon/sysmonLineGraph, isysmon/sysmonReport, sysmon.displaytypeconstants, sysmonChartArea, sysmonChartStackedArea, sysmonHistogram, sysmonLineGraph, sysmonReport
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: DisplayTypeConstants
req.redist: 
ms.custom: 19H1
f1_keywords:
 - eDisplayTypeConstant
 - isysmon/eDisplayTypeConstant
 - DisplayTypeConstants
 - isysmon/DisplayTypeConstants
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ISysmon.h
api_name:
 - DisplayTypeConstants
---

# DisplayTypeConstants enumeration


## -description

Determines how the performance counter data is graphed, for example, as a line graph or a histogram.

## -enum-fields

### -field sysmonLineGraph:1

Counter values are displayed in a line graph. Each marker on the line graph represents a data value.

### -field sysmonHistogram:2

Counter values are displayed as a histogram.

### -field sysmonReport:3

Counter values are displayed in a report format. Only the current value for each counter is displayed.

### -field sysmonChartArea:4

Counter values are displayed as a line graph. The area between the line and the x-axis is shaded. You can only use this option if the source of the counter data is a log file.

### -field sysmonChartStackedArea:5

Counter values are displayed as a line graph. The line graph for each counter is stacked one upon the other. The area between the line and the x-axis or adjacent counter is shaded. You can only use this option if the source of the counter data is a log file.

If the sum of all the counter values exceeds the maximum scale value of the graph, SYSMON uses an appropriate scale value for each counter in order to fit the counters within the maximum scale value of the graph.

## -remarks

The following enumeration values were introduced in Windows Vista.

<ul>
<li><b>sysmonChartArea</b></li>
<li><b>sysmonChartStackedArea</b></li>
</ul>

## -see-also

<a href="/windows/desktop/SysMon/systemmonitor-displaytype">SystemMonitor.DisplayType</a>
