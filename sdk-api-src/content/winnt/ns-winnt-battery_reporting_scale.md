---
UID: NS:winnt.BATTERY_REPORTING_SCALE
title: BATTERY_REPORTING_SCALE (winnt.h)
description: Contains the granularity of the battery capacity that is reported by IOCTL_BATTERY_QUERY_STATUS.
helpviewer_keywords: ["*PBATTERY_REPORTING_SCALE","BATTERY_REPORTING_SCALE","BATTERY_REPORTING_SCALE structure","PBATTERY_REPORTING_SCALE","PBATTERY_REPORTING_SCALE structure pointer","_win32_battery_reporting_scale_str","base.battery_reporting_scale_str","winnt/BATTERY_REPORTING_SCALE","winnt/PBATTERY_REPORTING_SCALE"]
old-location: base\battery_reporting_scale_str.htm
tech.root: base
ms.assetid: 91834159-e837-407b-8c9e-fbbcf9f208ef
ms.date: 12/05/2018
ms.keywords: '*PBATTERY_REPORTING_SCALE, BATTERY_REPORTING_SCALE, BATTERY_REPORTING_SCALE structure, PBATTERY_REPORTING_SCALE, PBATTERY_REPORTING_SCALE structure pointer, _win32_battery_reporting_scale_str, base.battery_reporting_scale_str, winnt/BATTERY_REPORTING_SCALE, winnt/PBATTERY_REPORTING_SCALE'
req.header: winnt.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: BATTERY_REPORTING_SCALE, *PBATTERY_REPORTING_SCALE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PBATTERY_REPORTING_SCALE
 - winnt/PBATTERY_REPORTING_SCALE
 - BATTERY_REPORTING_SCALE
 - winnt/BATTERY_REPORTING_SCALE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinNT.h
api_name:
 - BATTERY_REPORTING_SCALE
---

# BATTERY_REPORTING_SCALE structure


## -description

Contains the granularity of the battery capacity that is reported by <a href="/windows/desktop/Power/ioctl-battery-query-status">IOCTL_BATTERY_QUERY_STATUS</a>. A variable-length array of <b>BATTERY_REPORTING_SCALE</b> structures is returned from <a href="/windows/desktop/Power/ioctl-battery-query-information">IOCTL_BATTERY_QUERY_INFORMATION</a> when the <b>InformationLevel</b> is set to <b>BatteryGranularityInformation</b>.   Multiple entries are returned when the granularity depends on the present capacity of the battery.

## -struct-fields

### -field Granularity

The granularity of the capacity reading returned by <a href="/windows/desktop/Power/ioctl-battery-query-status">IOCTL_BATTERY_QUERY_STATUS</a> in milliwatt-hours (mWh).  Granularity may change over time as battery discharge and recharge lowers the range of readings.

### -field Capacity

The upper capacity limit for <i>Granularity</i>.   The value of <i>Granularity</i> is valid for capacities reported by <a href="/windows/desktop/Power/ioctl-battery-query-status">IOCTL_BATTERY_QUERY_STATUS</a> that are less than or equal to this capacity (mWh), but greater than or equal to the capacity given in the previous array element, or zero if this is the first array element.

## -remarks

The total number of <b>BATTERY_REPORTING_SCALE</b> entries returned from <a href="/windows/desktop/Power/ioctl-battery-query-information">IOCTL_BATTERY_QUERY_INFORMATION</a> is indicated by the value of the <i>lpBytesReturned</i> parameter of <a href="/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a>. To determine the number of elements in the array, divide the value of <i>lpBytesReturned</i> by the size of the 
<b>BATTERY_REPORTING_SCALE</b> structure. The maximum number of array entries that can be returned is four.

## -see-also

<a href="/windows/desktop/Power/ioctl-battery-query-information">IOCTL_BATTERY_QUERY_INFORMATION</a>



<a href="/windows/desktop/Power/ioctl-battery-query-status">IOCTL_BATTERY_QUERY_STATUS</a>

