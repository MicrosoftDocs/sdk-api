---
UID: NE:isysmon.eReportValueTypeConstant
title: eReportValueTypeConstant
author: windows-sdk-content
description: Determines if the Histogram and Report views graph the last value sampled or a calculated value using values from the sampling period, such as the average or minimum value.
old-location: sysmon\reportvaluetypeconstants.htm
old-project: SysMon
ms.assetid: 63287889-3928-4abf-a04d-6790fd70df83
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: ReportValueTypeConstants, ReportValueTypeConstants enumeration [SysMon], base.reportvaluetypeconstants, eReportValueTypeConstant, isysmon/ReportValueTypeConstants, isysmon/sysmonAverage, isysmon/sysmonCurrentValue, isysmon/sysmonDefaultValue, isysmon/sysmonMaximum, isysmon/sysmonMinimum, sysmon.reportvaluetypeconstants, sysmonAverage, sysmonCurrentValue, sysmonDefaultValue, sysmonMaximum, sysmonMinimum
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
req.typenames: ReportValueTypeConstants
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	ISysmon.h
api_name:
-	ReportValueTypeConstants
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
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
 

 

