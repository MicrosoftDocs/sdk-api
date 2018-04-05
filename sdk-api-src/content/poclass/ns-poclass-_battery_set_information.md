---
UID: NS:poclass._BATTERY_SET_INFORMATION
title: "_BATTERY_SET_INFORMATION"
author: windows-driver-content
description: Contains battery information to be set.
old-location: base\battery_set_information_str.htm
old-project: Power
ms.assetid: 535e56cb-2bab-458a-84a8-2d9a4d96412b
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: "*PBATTERY_SET_INFORMATION, BATTERY_SET_INFORMATION, BATTERY_SET_INFORMATION structure, BatteryCharge, BatteryCriticalBias, BatteryDischarge, PBATTERY_SET_INFORMATION, PBATTERY_SET_INFORMATION structure pointer, _BATTERY_SET_INFORMATION, _win32_battery_set_information_str, base.battery_set_information_str, batclass/BATTERY_SET_INFORMATION, batclass/PBATTERY_SET_INFORMATION, poclass/BATTERY_SET_INFORMATION, poclass/PBATTERY_SET_INFORMATION"
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
req.typenames: BATTERY_SET_INFORMATION, *PBATTERY_SET_INFORMATION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Poclass.h
-	Batclass.h
api_name:
-	BATTERY_SET_INFORMATION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# _BATTERY_SET_INFORMATION structure


## -description


Contains battery information to be set. This  structure is used with the 
<a href="https://msdn.microsoft.com/b827983d-5fb8-43f2-b732-541d16b3eb7b">IOCTL_BATTERY_SET_INFORMATION</a> control code.


## -struct-fields




### -field BatteryTag

The current battery tag for the battery. Information for a battery matching the tag can only be returned. Whenever this value does not match the battery's current tag, the IOCTL request will be completed with ERROR_FILE_NOT_FOUND, which indicates to the caller that the battery for which it has a tag for no longer exists. The caller may opt to use the 
<a href="https://msdn.microsoft.com/0bbe59ba-e037-47ce-a54a-6500ea7c9bc5">IOCTL_BATTERY_QUERY_TAG</a> operation to determine the tag of the newly installed battery, if one exists. (See 
<a href="https://msdn.microsoft.com/3580b37d-611c-46b4-9300-4943833d6852">Battery Tags</a> for more information.) 




When a query information request is made, this value is verified. In addition, if the request is in progress while this value changes, the request is aborted with the status of ERROR_FILE_NOT_FOUND.


### -field InformationLevel

The battery information to be set. The type of data in the <b>Buffer</b> member depends on the value of this member. This member can be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="BatteryCharge"></a><a id="batterycharge"></a><a id="BATTERYCHARGE"></a><dl>
<dt><b>BatteryCharge</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Informs the battery device that the user has requested that the battery should be charging at this time. For example, with a smart battery/charger/selector, the application could charge one battery at a time. The <b>Buffer</b> member of this structure is ignored.

</td>
</tr>
<tr>
<td width="40%"><a id="BatteryCriticalBias"></a><a id="batterycriticalbias"></a><a id="BATTERYCRITICALBIAS"></a><dl>
<dt><b>BatteryCriticalBias</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Sets the battery's critical bias adjustment. Note it is not envisioned that this value would normally be changed by software, and is present in the interfaces only as a maintenance feature. Not all batteries can maintain such a setting, and the battery information should be read to confirm that the battery accepted the setting.

</td>
</tr>
<tr>
<td width="40%"><a id="BatteryDischarge"></a><a id="batterydischarge"></a><a id="BATTERYDISCHARGE"></a><dl>
<dt><b>BatteryDischarge</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Informs the battery device that the user has requested that the battery be discharging at this time. For example, this could be used to indicate which battery the user currently wants to power the system. The <b>Buffer</b> member of this structure is ignored.

</td>
</tr>
</table>
 


### -field Buffer

The battery information to be set. The data depends on the value of <b>InformationLevel</b>.
					


## -remarks



The 
<b>BATTERY_SET_INFORMATION</b> structure is a variable-length structure, and you must allocate a buffer of suitable size for the information to be included in the structure.




## -see-also




<a href="https://msdn.microsoft.com/b827983d-5fb8-43f2-b732-541d16b3eb7b">IOCTL_BATTERY_SET_INFORMATION</a>
 

 

