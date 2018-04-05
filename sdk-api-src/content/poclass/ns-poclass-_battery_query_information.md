---
UID: NS:poclass._BATTERY_QUERY_INFORMATION
title: "_BATTERY_QUERY_INFORMATION"
author: windows-driver-content
description: Contains battery query information.
old-location: base\battery_query_information_str.htm
old-project: Power
ms.assetid: ef5466fe-7de8-48cd-ad48-5774d7a4bb46
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: "*PBATTERY_QUERY_INFORMATION, BATTERY_QUERY_INFORMATION, BATTERY_QUERY_INFORMATION structure, BatteryDeviceName, BatteryEstimatedTime, BatteryGranularityInformation, BatteryInformation, BatteryManufactureDate, BatteryManufactureName, BatterySerialNumber, BatteryTemperature, BatteryUniqueID, PBATTERY_QUERY_INFORMATION, PBATTERY_QUERY_INFORMATION structure pointer, _BATTERY_QUERY_INFORMATION, _win32_battery_query_information_str, base.battery_query_information_str, batclass/BATTERY_QUERY_INFORMATION, batclass/PBATTERY_QUERY_INFORMATION, poclass/BATTERY_QUERY_INFORMATION, poclass/PBATTERY_QUERY_INFORMATION"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: poclass.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Pnpxassoc.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: BATTERY_QUERY_INFORMATION, *PBATTERY_QUERY_INFORMATION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Poclass.h
-	Batclass.h
api_name:
-	BATTERY_QUERY_INFORMATION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# _BATTERY_QUERY_INFORMATION structure


## -description


Contains battery query information. This structure is used with the 
<a href="https://msdn.microsoft.com/4cc89b89-ab33-47c2-8327-9627cbd1595e">IOCTL_BATTERY_QUERY_INFORMATION</a> control code to specify the type of information to return.


## -struct-fields




### -field BatteryTag

The current battery tag for the battery. Only information for a battery matching the tag can be returned. Whenever this value does not match the battery's current tag, the IOCTL request will be completed with ERROR_FILE_NOT_FOUND. This indicates to the caller that the battery associated with the tag longer exists. The caller may opt to use the 
<a href="https://msdn.microsoft.com/0bbe59ba-e037-47ce-a54a-6500ea7c9bc5">IOCTL_BATTERY_QUERY_TAG</a> operation to determine the tag of the newly installed battery, if one exists. (See 
<a href="https://msdn.microsoft.com/3580b37d-611c-46b4-9300-4943833d6852">Battery Tags</a> for more information.) 




When a query information request is made, this value is verified. In addition, if the request is in progress while this value changes, the request is aborted with the status of ERROR_FILE_NOT_FOUND.


### -field InformationLevel

The level of the battery information being queried. The data returned by the IOCTL depends on this value. This member can be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="BatteryDeviceName"></a><a id="batterydevicename"></a><a id="BATTERYDEVICENAME"></a><dl>
<dt><b>BatteryDeviceName</b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
Null-terminated Unicode string that contains the battery's name.

</td>
</tr>
<tr>
<td width="40%"><a id="BatteryEstimatedTime"></a><a id="batteryestimatedtime"></a><a id="BATTERYESTIMATEDTIME"></a><dl>
<dt><b>BatteryEstimatedTime</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
A <b>ULONG</b> that specifies the estimated battery run time, in seconds. If the rate of drain provided in the <b>AtRate</b> member of the 
<b>BATTERY_QUERY_INFORMATION</b> structure is zero, this calculation is based on the present rate of drain. If <b>AtRate</b> is nonzero, the time returned is the expected run time for the given rate. If the estimated time is unknown (for example, the battery is not discharging and the <b>AtRate</b> specified was zero), the return value is BATTERY_UNKNOWN_TIME. Note that this value is not very accurate on some battery systems, and may vary widely depending on present power usage, which could be affected by disk activity and other factors. There is no notification mechanism for changes in this value.

</td>
</tr>
<tr>
<td width="40%"><a id="BatteryGranularityInformation"></a><a id="batterygranularityinformation"></a><a id="BATTERYGRANULARITYINFORMATION"></a><dl>
<dt><b>BatteryGranularityInformation</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
An array of 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff536289">BATTERY_REPORTING_SCALE</a> structures, never more than four entries.

</td>
</tr>
<tr>
<td width="40%"><a id="BatteryInformation"></a><a id="batteryinformation"></a><a id="BATTERYINFORMATION"></a><dl>
<dt><b>BatteryInformation</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
A 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff536283">BATTERY_INFORMATION</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="BatteryManufactureDate"></a><a id="batterymanufacturedate"></a><a id="BATTERYMANUFACTUREDATE"></a><dl>
<dt><b>BatteryManufactureDate</b></dt>
<dt>5</dt>
</dl>
</td>
<td width="60%">
A 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff536284">BATTERY_MANUFACTURE_DATE</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="BatteryManufactureName"></a><a id="batterymanufacturename"></a><a id="BATTERYMANUFACTURENAME"></a><dl>
<dt><b>BatteryManufactureName</b></dt>
<dt>6</dt>
</dl>
</td>
<td width="60%">
Null-terminated Unicode string that specifies the name of the manufacturer of the battery.

</td>
</tr>
<tr>
<td width="40%"><a id="BatterySerialNumber"></a><a id="batteryserialnumber"></a><a id="BATTERYSERIALNUMBER"></a><dl>
<dt><b>BatterySerialNumber</b></dt>
<dt>8</dt>
</dl>
</td>
<td width="60%">
Null-terminated Unicode string that specifies the battery's serial number.

</td>
</tr>
<tr>
<td width="40%"><a id="BatteryTemperature"></a><a id="batterytemperature"></a><a id="BATTERYTEMPERATURE"></a><dl>
<dt><b>BatteryTemperature</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
A <b>ULONG</b> that specifies the battery's current temperature, in 10ths of a degree Kelvin.

</td>
</tr>
<tr>
<td width="40%"><a id="BatteryUniqueID"></a><a id="batteryuniqueid"></a><a id="BATTERYUNIQUEID"></a><dl>
<dt><b>BatteryUniqueID</b></dt>
<dt>7</dt>
</dl>
</td>
<td width="60%">
Null-terminated Unicode string that uniquely identifies the battery. This value can be used to track a specific battery. In the case of smart batteries, this ID would be the concatenation of the manufacturer's name, device name, date of manufacture, and a printable representation of the serial number. 




This value is not intended to be displayed to the user.

</td>
</tr>
</table>
 


### -field AtRate

This member is used only if <b>InformationLevel</b> is BatteryEstimatedTime. 




If this member is nonzero, it is a rate of drain that will be used to calculate the time until the battery is discharged for the BatteryEstimatedTime of an individual battery. It must be specified in mW, and must be a negative value to represent a battery discharge rate.


## -remarks



Some information about batteries is optional or may be meaningless for some batteries. If the particular type of data requested is not available for the current battery, then ERROR_INVALID_FUNCTION is returned.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff536283">BATTERY_INFORMATION</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff536284">BATTERY_MANUFACTURE_DATE</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff536289">BATTERY_REPORTING_SCALE</a>



<a href="https://msdn.microsoft.com/4cc89b89-ab33-47c2-8327-9627cbd1595e">IOCTL_BATTERY_QUERY_INFORMATION</a>



<a href="https://msdn.microsoft.com/0bbe59ba-e037-47ce-a54a-6500ea7c9bc5">IOCTL_BATTERY_QUERY_TAG</a>
 

 

