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
 

 

