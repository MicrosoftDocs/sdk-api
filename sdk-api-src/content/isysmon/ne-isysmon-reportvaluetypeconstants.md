---
UID: NE:isysmon.eReportValueTypeConstant
title: ReportValueTypeConstants (isysmon.h)
description: Determines if the Histogram and Report views graph the last value sampled or a calculated value using values from the sampling period, such as the average or minimum value.
helpviewer_keywords: ["ReportValueTypeConstants","ReportValueTypeConstants enumeration [SysMon]","base.reportvaluetypeconstants","isysmon/ReportValueTypeConstants","isysmon/sysmonAverage","isysmon/sysmonCurrentValue","isysmon/sysmonDefaultValue","isysmon/sysmonMaximum","isysmon/sysmonMinimum","sysmon.reportvaluetypeconstants","sysmonAverage","sysmonCurrentValue","sysmonDefaultValue","sysmonMaximum","sysmonMinimum"]
old-location: sysmon\reportvaluetypeconstants.htm
tech.root: SysMon
ms.assetid: 63287889-3928-4abf-a04d-6790fd70df83
ms.date: 12/05/2018
ms.keywords: ReportValueTypeConstants, ReportValueTypeConstants enumeration [SysMon], base.reportvaluetypeconstants, isysmon/ReportValueTypeConstants, isysmon/sysmonAverage, isysmon/sysmonCurrentValue, isysmon/sysmonDefaultValue, isysmon/sysmonMaximum, isysmon/sysmonMinimum, sysmon.reportvaluetypeconstants, sysmonAverage, sysmonCurrentValue, sysmonDefaultValue, sysmonMaximum, sysmonMinimum
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
req.typenames: ReportValueTypeConstants
req.redist: 
ms.custom: 19H1
f1_keywords:
 - eReportValueTypeConstant
 - isysmon/eReportValueTypeConstant
 - ReportValueTypeConstants
 - isysmon/ReportValueTypeConstants
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
 - ReportValueTypeConstants
---

# ReportValueTypeConstants enumeration


## -description

Determines if the Histogram and Report views graph the last value sampled or a calculated value using values from the sampling period, such as the average or minimum value.

## -enum-fields

### -field sysmonDefaultValue:0

The value displayed depends on the source of the counter data. If the source of the counter data is from the current activity of the computer, <b>sysmonCurrentValue</b> is used. If the source of the counter data is a log file, <b>sysmonAverage</b> is used.

### -field sysmonCurrentValue:0x1

The current value of the counter.

### -field sysmonAverage:0x2

The average value of the counter over the sampling period.

### -field sysmonMinimum:0x3

The minimum value of the counter over the sampling period.

### -field sysmonMaximum:0x4

The maximum value of the counter over the sampling period.

## -see-also

<a href="/windows/desktop/SysMon/systemmonitor-reportvaluetype">SystemMonitor.ReportValueType</a>
