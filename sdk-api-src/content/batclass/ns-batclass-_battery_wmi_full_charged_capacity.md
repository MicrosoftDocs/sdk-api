---
UID: NS:batclass._BATTERY_WMI_FULL_CHARGED_CAPACITY
title: "_BATTERY_WMI_FULL_CHARGED_CAPACITY"
author: windows-sdk-content
description: Defines information about the capacity of a battery for use with the BatteryClassQueryWmiDataBlock).
old-location: battery\battery_wmi_full_charged_capacity.htm
tech.root: battery
ms.assetid: BE01DF36-71A8-464A-977B-499325DDB37E
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: "*PBATTERY_WMI_FULL_CHARGED_CAPACITY, BATTERY_WMI_FULL_CHARGED_CAPACITY, BATTERY_WMI_FULL_CHARGED_CAPACITY structure [Battery Devices], PBATTERY_WMI_FULL_CHARGED_CAPACITY, PBATTERY_WMI_FULL_CHARGED_CAPACITY structure pointer [Battery Devices], _BATTERY_WMI_FULL_CHARGED_CAPACITY, batclass/BATTERY_WMI_FULL_CHARGED_CAPACITY, batclass/PBATTERY_WMI_FULL_CHARGED_CAPACITY, battery.battery_wmi_full_charged_capacity"
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Batclass.h
api_name:
 - BATTERY_WMI_FULL_CHARGED_CAPACITY
product: Windows
targetos: Windows
req.typenames: BATTERY_WMI_FULL_CHARGED_CAPACITY, *PBATTERY_WMI_FULL_CHARGED_CAPACITY
req.redist: 
---

# _BATTERY_WMI_FULL_CHARGED_CAPACITY structure


## -description


Defines information about the capacity of a battery for use with the <a href="https://msdn.microsoft.com/2a5c4c14-fc80-4a0a-b447-6fe33ff1d42f">BatteryClassQueryWmiDataBlock</a>)


## -struct-fields




### -field Tag

A tag that identifies a specific battery.


### -field FullChargedCapacity

The  current fully charged capacity, measured for example in milliwatt-hours, of a battery. If BATTERY_CAPACITY_RELATIVE is set, the units are undefined. For more information see the <a href="https://msdn.microsoft.com/e9326d96-bd96-4493-a0b2-abe6b8f2401a">BATTERY_INFORMATION</a>.


## -see-also




<a href="https://msdn.microsoft.com/2a5c4c14-fc80-4a0a-b447-6fe33ff1d42f">BatteryClassQueryWmiDataBlock</a>
 

 

