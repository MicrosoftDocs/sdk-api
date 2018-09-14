---
UID: NS:winnt.BATTERY_REPORTING_SCALE
title: BATTERY_REPORTING_SCALE
author: windows-sdk-content
description: Contains the granularity of the battery capacity that is reported by IOCTL_BATTERY_QUERY_STATUS.
old-location: base\battery_reporting_scale_str.htm
tech.root: power
ms.assetid: 91834159-e837-407b-8c9e-fbbcf9f208ef
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: "*PBATTERY_REPORTING_SCALE, BATTERY_REPORTING_SCALE, BATTERY_REPORTING_SCALE structure, PBATTERY_REPORTING_SCALE, PBATTERY_REPORTING_SCALE structure pointer, _win32_battery_reporting_scale_str, base.battery_reporting_scale_str, winnt/BATTERY_REPORTING_SCALE, winnt/PBATTERY_REPORTING_SCALE"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinNT.h
api_name:
 - BATTERY_REPORTING_SCALE
product: Windows
targetos: Windows
req.typenames: BATTERY_REPORTING_SCALE, *PBATTERY_REPORTING_SCALE
req.redist: 
---

# BATTERY_REPORTING_SCALE structure


## -description


Contains the granularity of the battery capacity that is reported by <a href="https://msdn.microsoft.com/7a7bf429-9b2c-4faf-9f27-fb5fd8dd18df">IOCTL_BATTERY_QUERY_STATUS</a>. A variable-length array of <b>BATTERY_REPORTING_SCALE</b> structures is returned from <a href="https://msdn.microsoft.com/4cc89b89-ab33-47c2-8327-9627cbd1595e">IOCTL_BATTERY_QUERY_INFORMATION</a> when the <b>InformationLevel</b> is set to <b>BatteryGranularityInformation</b>.   Multiple entries are returned when the granularity depends on the present capacity of the battery.
		


## -struct-fields




### -field Granularity

The granularity of the capacity reading returned by <a href="https://msdn.microsoft.com/7a7bf429-9b2c-4faf-9f27-fb5fd8dd18df">IOCTL_BATTERY_QUERY_STATUS</a> in milliwatt-hours (mWh).  Granularity may change over time as battery discharge and recharge lowers the range of readings.


### -field Capacity

The upper capacity limit for <i>Granularity</i>.   The value of <i>Granularity</i> is valid for capacities reported by <a href="https://msdn.microsoft.com/7a7bf429-9b2c-4faf-9f27-fb5fd8dd18df">IOCTL_BATTERY_QUERY_STATUS</a> that are less than or equal to this capacity (mWh), but greater than or equal to the capacity given in the previous array element, or zero if this is the first array element.


## -remarks



The total number of <b>BATTERY_REPORTING_SCALE</b> entries returned from <a href="https://msdn.microsoft.com/4cc89b89-ab33-47c2-8327-9627cbd1595e">IOCTL_BATTERY_QUERY_INFORMATION</a> is indicated by the value of the <i>lpBytesReturned</i> parameter of <a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a>. To determine the number of elements in the array, divide the value of <i>lpBytesReturned</i> by the size of the 
<b>BATTERY_REPORTING_SCALE</b> structure. The maximum number of array entries that can be returned is four.




## -see-also




<a href="https://msdn.microsoft.com/4cc89b89-ab33-47c2-8327-9627cbd1595e">IOCTL_BATTERY_QUERY_INFORMATION</a>



<a href="https://msdn.microsoft.com/7a7bf429-9b2c-4faf-9f27-fb5fd8dd18df">IOCTL_BATTERY_QUERY_STATUS</a>
 

 

