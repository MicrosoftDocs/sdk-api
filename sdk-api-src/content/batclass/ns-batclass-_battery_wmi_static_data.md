---
UID: NS:batclass._BATTERY_WMI_STATIC_DATA
title: "_BATTERY_WMI_STATIC_DATA"
author: windows-sdk-content
description: Defines static data about a battery.
old-location: battery\battery_wmi_static_data.htm
old-project: battery
ms.assetid: 39930853-AB5A-4DA5-A544-7913770C4D88
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: "*PBATTERY_WMI_STATIC_DATA, BATTERY_WMI_STATIC_DATA, BATTERY_WMI_STATIC_DATA structure [Battery Devices], PBATTERY_WMI_STATIC_DATA, PBATTERY_WMI_STATIC_DATA structure pointer [Battery Devices], _BATTERY_WMI_STATIC_DATA, batclass/BATTERY_WMI_STATIC_DATA, batclass/PBATTERY_WMI_STATIC_DATA, battery.battery_wmi_static_data"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: batclass.h
req.include-header: Batclass.h
req.target-type: Windows
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
tech.root: 
req.typenames: BATTERY_WMI_STATIC_DATA, *PBATTERY_WMI_STATIC_DATA
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Batclass.h
api_name:
-	BATTERY_WMI_STATIC_DATA
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _BATTERY_WMI_STATIC_DATA structure


## -description


Defines static data about a battery.


## -struct-fields




### -field Tag

A tag that identifies a specific battery.


### -field ManufactureDate

 


### -field Granularity

Specifies the granularity as a <a href="https://msdn.microsoft.com/library/windows/hardware/ff536289">BATTERY_REPORTING_SCALE</a> value.


### -field Capabilities

Battery capabilities as a ULONG value encoded with one or more of the following flags: 







#### BATTERY_SYSTEM_BATTERY

Set this flag if the battery can provide general power to run the system.



#### BATTERY_CAPACITY_RELATIVE

Set this flag if the miniclass driver will report battery capacity and rate as a percentage of total capacity and rate rather than as absolute values. Otherwise, the miniclass driver should report capacity in milliwatt-hours and rate in milliwatts.



#### BATTERY_IS_SHORT_TERM

Set this flag if the battery is a UPS, intended for short-term, failsafe use. Clear the flag for any other type of device.



#### BATTERY_SET_CHARGE_SUPPORTED

Set this flag if the miniclass driver supports the <b>BatteryCharge </b>setting in calls to <i>BatteryMiniSetInformation</i>.



#### BATTERY_SET_DISCHARGE_SUPPORTED

Set this flag if the miniclass driver supports the <b>BatteryDischarge </b>setting in calls to <i>BatteryMiniSetInformation</i>.


### -field Technology

Specify zero for a primary, nonrechargeable battery, or one for a secondary, rechargeable battery.


### -field Chemistry

A four-character string indicating the type of chemistry used in the battery. Possible values include "PbAc" (Lead Acid), "LION" (Lithium Ion), "NiCd" (Nickel Cadmium), "NiMH" (Nickel Metal Hydride), "NiZn" (Nickel Zinc), and "RAM" (Rechargeable Alkaline-Manganese). Additional values might be returned as additional battery types become available.


### -field DesignedCapacity

The theoretical capacity of the battery when new, in milliwatt-hours. If BATTERY_CAPACITY_RELATIVE is set, the units are undefined.


### -field DefaultAlert1

The capacity, in milliwatt-hours, at which a low battery alert should occur. 


### -field DefaultAlert2

The capacity, in milliwatt-hours, at which a warning battery alert should occur.


### -field CriticalBias

Specify the amount, in milliwatt-hours, of any small reserved charge that remains when the critical battery level shows zero. Miniclass drivers should subtract this value from the battery's <b>FullChargedCapacity</b> and remaining capacity, which is reported in <a href="https://msdn.microsoft.com/library/windows/hardware/ff536290">BATTERY_STATUS</a>, before reporting those values.


### -field Strings

Four variable length string values are stored with the first USHORT value containing the length of the string in bytes.


#### - WCHAR

A <a href="https://msdn.microsoft.com/library/windows/hardware/ff536284">BATTERY_MANUFACTURE_DATE</a> structure that specifies the date that the battery was manufactured. 


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff536284">BATTERY_MANUFACTURE_DATE</a>
 

 

