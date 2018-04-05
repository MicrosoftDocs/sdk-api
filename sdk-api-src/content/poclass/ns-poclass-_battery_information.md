---
UID: NS:poclass._BATTERY_INFORMATION
title: "_BATTERY_INFORMATION"
author: windows-driver-content
description: Contains battery information.
old-location: base\battery_information_str.htm
old-project: Power
ms.assetid: 6a236f48-5a06-4537-a769-bd68e5c0eb27
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: "*PBATTERY_INFORMATION, BATTERY_CAPACITY_RELATIVE, BATTERY_INFORMATION, BATTERY_INFORMATION structure, BATTERY_IS_SHORT_TERM, BATTERY_SET_CHARGE_SUPPORTED, BATTERY_SET_DISCHARGE_SUPPORTED, BATTERY_SYSTEM_BATTERY, LION, Li-I, NiCd, NiMH, NiZn, PBATTERY_INFORMATION, PBATTERY_INFORMATION structure pointer, PbAc, RAM, _BATTERY_INFORMATION, _win32_battery_information_str, base.battery_information_str, batclass/BATTERY_INFORMATION, batclass/PBATTERY_INFORMATION, poclass/BATTERY_INFORMATION, poclass/PBATTERY_INFORMATION"
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
req.typenames: BATTERY_INFORMATION, *PBATTERY_INFORMATION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Poclass.h
-	Batclass.h
api_name:
-	BATTERY_INFORMATION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# _BATTERY_INFORMATION structure


## -description


Contains battery information. This structure is returned by the 
<a href="https://msdn.microsoft.com/4cc89b89-ab33-47c2-8327-9627cbd1595e">IOCTL_BATTERY_QUERY_INFORMATION</a> control code when the BatteryInformation information level is requested.


## -struct-fields




### -field Capabilities

The battery capabilities. This member can be one or more of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="BATTERY_CAPACITY_RELATIVE"></a><a id="battery_capacity_relative"></a><dl>
<dt><b>BATTERY_CAPACITY_RELATIVE</b></dt>
<dt>0x40000000</dt>
</dl>
</td>
<td width="60%">
Indicates that the battery capacity and rate information are relative, and not in any specific units.  If this bit is not set, the reporting units are milliwatt-hours (mWh) for capacity and milliwatts (mW) for rate.  If this bit is set, all references to units in the other battery documentation can be ignored.  All rate information is reported in units per hour.  For example, if the fully charged capacity is reported as 100, a rate of 200  indicates that the battery will use all of its capacity in half an hour.

</td>
</tr>
<tr>
<td width="40%"><a id="BATTERY_IS_SHORT_TERM"></a><a id="battery_is_short_term"></a><dl>
<dt><b>BATTERY_IS_SHORT_TERM</b></dt>
<dt>0x20000000</dt>
</dl>
</td>
<td width="60%">
Indicates that the normal operation is for a fail-safe function. If this bit is not set the battery is expected to be used during normal system usage.

</td>
</tr>
<tr>
<td width="40%"><a id="BATTERY_SET_CHARGE_SUPPORTED"></a><a id="battery_set_charge_supported"></a><dl>
<dt><b>BATTERY_SET_CHARGE_SUPPORTED</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Indicates that set information requests of the type BatteryCharge are supported by this battery device.

</td>
</tr>
<tr>
<td width="40%"><a id="BATTERY_SET_DISCHARGE_SUPPORTED"></a><a id="battery_set_discharge_supported"></a><dl>
<dt><b>BATTERY_SET_DISCHARGE_SUPPORTED</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
Indicates that set information requests of the type BatteryDischarge are supported by this battery device.

</td>
</tr>
<tr>
<td width="40%"><a id="BATTERY_SYSTEM_BATTERY"></a><a id="battery_system_battery"></a><dl>
<dt><b>BATTERY_SYSTEM_BATTERY</b></dt>
<dt>0x80000000</dt>
</dl>
</td>
<td width="60%">
Indicates that the battery can provide general power to run the system.

</td>
</tr>
</table>
 


### -field Technology

The battery technology. This member can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Nonrechargeable battery, for example, alkaline.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Rechargeable battery, for example, lead acid.

</td>
</tr>
</table>
 


### -field Reserved

Reserved.


### -field Chemistry

An abbreviated character string that indicates the battery's chemistry. This string is not necessarily zero-terminated. The following is a partial list of abbreviations that can be returned and the associated chemistries. 



<table>
<tr>
<th>Unicode string</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PbAc"></a><a id="pbac"></a><a id="PBAC"></a><dl>
<dt><b>PbAc</b></dt>
</dl>
</td>
<td width="60%">
Lead Acid

</td>
</tr>
<tr>
<td width="40%"><a id="LION"></a><a id="lion"></a><dl>
<dt><b>LION</b></dt>
</dl>
</td>
<td width="60%">
Lithium Ion

</td>
</tr>
<tr>
<td width="40%"><a id="Li-I"></a><a id="li-i"></a><a id="LI-I"></a><dl>
<dt><b>Li-I</b></dt>
</dl>
</td>
<td width="60%">
Lithium Ion

</td>
</tr>
<tr>
<td width="40%"><a id="NiCd"></a><a id="nicd"></a><a id="NICD"></a><dl>
<dt><b>NiCd</b></dt>
</dl>
</td>
<td width="60%">
Nickel Cadmium

</td>
</tr>
<tr>
<td width="40%"><a id="NiMH"></a><a id="nimh"></a><a id="NIMH"></a><dl>
<dt><b>NiMH</b></dt>
</dl>
</td>
<td width="60%">
Nickel Metal Hydride

</td>
</tr>
<tr>
<td width="40%"><a id="NiZn"></a><a id="nizn"></a><a id="NIZN"></a><dl>
<dt><b>NiZn</b></dt>
</dl>
</td>
<td width="60%">
Nickel Zinc

</td>
</tr>
<tr>
<td width="40%"><a id="RAM"></a><a id="ram"></a><dl>
<dt><b>RAM</b></dt>
</dl>
</td>
<td width="60%">
Rechargeable Alkaline-Manganese

</td>
</tr>
</table>
 

Other chemistries may appear in the future and your code should be able to handle them.


### -field DesignedCapacity

The theoretical capacity of the battery when new, in mWh unless BATTERY_CAPACITY_RELATIVE is set. In that case, the units are undefined.


### -field FullChargedCapacity

The battery's current fully charged capacity in mWh (or relative). Compare this value to <b>DesignedCapacity</b> to estimate the battery's wear.


### -field DefaultAlert1

The manufacturer's suggested capacity, in mWh, at which a low battery alert should occur. Definitions of low vary from manufacturer to manufacturer. In general, a warning state will occur before a low state, but you should not assume that it always will.  To reduce risk of data loss, this value is usually used as the default setting for the critical battery alarm.




### -field DefaultAlert2

The manufacturer's suggested capacity, in mWh, at which a warning battery alert should occur. Definitions of warning vary from manufacturer to manufacturer. In general, a warning state will occur before a low state, but you should not assume that it always will.  To reduce risk of data loss, this value is usually used as the default setting for the low battery alarm.




### -field CriticalBias

A bias from zero, in mWh, which is applied to battery reporting. Some batteries reserve a small charge that is biased out of the battery's capacity values to show "0" as the critical battery level. Critical bias is analogous to setting a fuel gauge to show "empty" when there are several liters of fuel left.


### -field CycleCount

The number of charge/discharge cycles the battery has experienced. This provides a means to determine the battery's wear. If the battery does not support a cycle counter, this member is zero.


## -remarks



Generally, a warning state occurs before a low state, but you should not assume it will. It is possible to poll a battery and find that neither alert level has occurred, and poll the battery again and find it discharged to the extent that both levels have been achieved. This may indicate that you are not polling often enough. It may also indicate that the battery is unable to hold a charge for very long and is discharging more rapidly than you expected. Such a battery may be nearing the end of its useful life, or it may be damaged.




## -see-also




<a href="https://msdn.microsoft.com/4cc89b89-ab33-47c2-8327-9627cbd1595e">IOCTL_BATTERY_QUERY_INFORMATION</a>
 

 

