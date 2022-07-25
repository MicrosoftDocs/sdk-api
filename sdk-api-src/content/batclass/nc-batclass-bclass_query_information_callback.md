---
UID: NC:batclass.BCLASS_QUERY_INFORMATION_CALLBACK
title: BCLASS_QUERY_INFORMATION_CALLBACK (batclass.h)
description: BatteryMiniQueryInformation returns information about the given battery device.
helpviewer_keywords: ["BCLASS_QUERY_INFORMATION_CALLBACK","BCLASS_QUERY_INFORMATION_CALLBACK callback","BatteryMiniQueryInformation","BatteryMiniQueryInformation callback function [Battery Devices]","bat-mini_89cb050e-0a2e-4fad-b6fa-c2977703c782.xml","batclass/BatteryMiniQueryInformation","battery.batteryminiqueryinformation"]
old-location: battery\batteryminiqueryinformation.htm
tech.root: battery
ms.assetid: bd96b79a-5670-4aaf-b72c-619818c2a2e7
ms.date: 12/05/2018
ms.keywords: BCLASS_QUERY_INFORMATION_CALLBACK, BCLASS_QUERY_INFORMATION_CALLBACK callback, BatteryMiniQueryInformation, BatteryMiniQueryInformation callback function [Battery Devices], bat-mini_89cb050e-0a2e-4fad-b6fa-c2977703c782.xml, batclass/BatteryMiniQueryInformation, battery.batteryminiqueryinformation
req.header: batclass.h
req.include-header: Batclass.h
req.target-type: Desktop
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
req.lib: 
req.dll: 
req.irql: PASSIVE_LEVEL
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - BCLASS_QUERY_INFORMATION_CALLBACK
 - batclass/BCLASS_QUERY_INFORMATION_CALLBACK
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Batclass.h
api_name:
 - BatteryMiniQueryInformation
---

# BCLASS_QUERY_INFORMATION_CALLBACK callback function


## -description

<i>BatteryMiniQueryInformation</i> returns information about the given battery device.

## -parameters

### -param Context [in]

A pointer to the context area allocated by the miniclass driver for the battery device.

### -param BatteryTag [in]

A pointer to a battery tag previously returned by <i>BatteryMiniQueryTag</i>.

### -param Level [in]

The type of battery information to be returned. Possible values are:

<b>BatteryInformation</b>
<b>BatteryGranularityInformation</b>
<b>BatteryTemperature</b>
<b>BatteryEstimatedTime</b>
<b>BatteryDeviceName</b>
<b>BatteryManufactureDate</b>
<b>BatteryManufactureName</b>
<b>BatteryUniqueID</b>
<b>BatterySerialNumber</b>

### -param AtRate [in]

The rate of drain, in negative milliwatts, used to calculate the time to discharge the battery. This parameter is meaningful only when <i>Level</i> is <b>BatteryEstimatedTime</b>; this parameter is ignored for all other values of <i>Level</i>.

### -param Buffer [out]

A pointer to a buffer that is allocated by the battery class driver. The buffer is used to return the requested information. The buffer is used to return the requested information. Miniclass drivers format the contents of the buffer depending upon the value of <i>Level</i>, as follows:





#### BatteryInformation

Return information formatted as a BATTERY_INFORMATION structure. 



#### BatteryGranularityInformation

Return a variable-length array of type BATTERY_REPORTING_SCALE that contains the reporting granularity of the remaining capacity. The number of entries returned depends upon the size of the returned buffer, to a maximum of four entries per battery. 



#### BatteryTemperature

Return a ULONG value giving the current temperature of the battery, in tenths of a degree Kelvin. 



#### BatteryEstimatedTime

Return a ULONG value estimating the number of seconds of run time remaining on the battery, based on the rate of drain specified in <i>AtRate</i>. If <i>AtRate</i> is negative or zero, the miniclass driver should calculate the run time based on the current rate of drain. However, if the driver cannot make an estimate (for example, <i>AtRate</i> is zero and the battery is not discharging), it should return BATTERY_UNKNOWN_TIME.



#### BatteryDeviceName

Return a Unicode string specifying the name of the battery. For example, DR202 identifies a Duracell smart battery.



#### BatteryManufactureDate

Return a BATTERY_MANUFACTURE_DATE structure specifying the date the battery was manufactured. 



#### BatteryManufactureName

Return a Unicode string specifying the model name given to the battery by its manufacturer. 



#### BatteryUniqueID

Return a Unicode string that uniquely identifies the battery, typically a concatenation of the battery's manufacturer, date, and serial number. 



#### BatterySerialNumber

Return a Unicode string that contains the battery's serial number.

### -param BufferLength [in]

The length, in bytes, of the buffer pointed to by <i>Buffer</i>.

### -param ReturnedLength [out]

The number of bytes returned in the buffer pointed to by <i>Buffer</i>.

## -returns

<i>BatteryMiniQueryInformation</i> returns one of the following:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The battery designated by <i>BatteryTag</i> is currently installed and the requested information has been returned. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_NO_SUCH_DEVICE</b></dt>
</dl>
</td>
<td width="60%">
The battery designated by <i>BatteryTag</i> is not present.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_INVALID_DEVICE_REQUEST</b></dt>
</dl>
</td>
<td width="60%">
The <i>Level</i> parameter specifies information that this battery does not support.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The <i>Level </i> parameter is not one of the enumerators listed.

</td>
</tr>
</table>

## -remarks

The battery class driver calls a miniclass driver's <i>BatteryMiniQueryInformation</i> routine to get various types of information about the battery. The information returned depends upon the <i>Level </i> parameter. Not all batteries support all the possible types of information that the class driver might request. Miniclass drivers should return STATUS_INVALID_DEVICE_REQUEST for any such requests.

If <i>Level </i> specifies <b>BatteryInformation</b>, the miniclass driver must return a BATTERY_INFORMATION structure in the buffer pointed to by <i>Buffer</i>. This structure contains status information about the battery, including its capabilities, technology (whether the battery is rechargeable), and chemistry; theoretical and actual full-charged capacity; critical bias; number of charge/discharge cycles; and the capacity levels at which warning alerts occur.

If <i>Level </i> specifies <b>BatteryGranularityInformation</b>, the miniclass driver can return an array of one to four elements, formatted as BATTERY_REPORTING_SCALE structures. Each element of the array consists of a granularity value and a remaining capacity value, in milliwatt-hours. The granularity indicates the precision of measurement and thus is an indicator of the accuracy of the capacity. 

Most types of batteries report capacity on a single scale. Miniclass drivers for these batteries return only one entry, giving the remaining capacity and the precision of the scale. Some batteries, however, have two scales: a gross scale that measures whether capacity is greater or less than fifty percent, and a finer scale that applies as capacity approaches zero. Miniclass drivers for such batteries should return two entries describing the two scales.

If <i>Level</i> specifies <b>BatteryEstimatedTime</b>, the miniclass driver must use the optional <i>AtRate </i> parameter to estimate the amount of time remaining to use the battery. The <i>AtRate</i> parameter specifies a drain rate, in negative milliwatts. 

If <i>Level</i> specifies <b>BatteryUniqueId</b>, the miniclass driver must return a string that uniquely identifies this particular battery. For control method and smart batteries, the unique ID is the concatenation of the manufacture name, the device name, the manufacture date, and the ASCII representation of the battery's serial number. This value is not meant to be displayed.

## -see-also

<a href="/previous-versions/ff536283(v=vs.85)">BATTERY_INFORMATION</a>



<a href="/previous-versions/ff536284(v=vs.85)">BATTERY_MANUFACTURE_DATE</a>



<a href="/windows-hardware/drivers/ddi/content/wdm/ns-wdm-battery_reporting_scale">BATTERY_REPORTING_SCALE</a>