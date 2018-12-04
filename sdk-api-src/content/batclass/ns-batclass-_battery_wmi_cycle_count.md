---
UID: NS:batclass._BATTERY_WMI_CYCLE_COUNT
title: "_BATTERY_WMI_CYCLE_COUNT"
author: windows-sdk-content
description: Defines information about number of charge cycles of a battery for use with the BatteryClassQueryWmiDataBlock function.
old-location: battery\battery_wmi_cycle_count.htm
tech.root: battery
ms.assetid: DFC94773-C198-4FC4-813C-0986ABA953A5
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: "*PBATTERY_WMI_CYCLE_COUNT, BATTERY_WMI_CYCLE_COUNT, BATTERY_WMI_CYCLE_COUNT structure [Battery Devices], PBATTERY_WMI_CYCLE_COUNT, PBATTERY_WMI_CYCLE_COUNT structure pointer [Battery Devices], _BATTERY_WMI_CYCLE_COUNT, batclass/BATTERY_WMI_CYCLE_COUNT, batclass/PBATTERY_WMI_CYCLE_COUNT, battery.battery_wmi_cycle_count"
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
 - BATTERY_WMI_CYCLE_COUNT
product: Windows
targetos: Windows
req.typenames: BATTERY_WMI_CYCLE_COUNT, *PBATTERY_WMI_CYCLE_COUNT
req.redist: 
---

# _BATTERY_WMI_CYCLE_COUNT structure


## -description


Defines information about number of charge cycles of a battery for use with the <a href="https://msdn.microsoft.com/2a5c4c14-fc80-4a0a-b447-6fe33ff1d42f">BatteryClassQueryWmiDataBlock</a> function.


## -struct-fields




### -field Tag

A tag that identifies a specific battery.


### -field CycleCount

The number of charge/discharge cycles the battery has experienced, or zero if the battery does not support a cycle counter.


## -see-also




<a href="https://msdn.microsoft.com/2a5c4c14-fc80-4a0a-b447-6fe33ff1d42f">BatteryClassQueryWmiDataBlock</a>
 

 

