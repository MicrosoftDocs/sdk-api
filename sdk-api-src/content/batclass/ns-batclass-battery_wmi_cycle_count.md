---
UID: NS:batclass._BATTERY_WMI_CYCLE_COUNT
title: BATTERY_WMI_CYCLE_COUNT (batclass.h)
description: Defines information about number of charge cycles of a battery for use with the BatteryClassQueryWmiDataBlock function.
helpviewer_keywords: ["*PBATTERY_WMI_CYCLE_COUNT","BATTERY_WMI_CYCLE_COUNT","BATTERY_WMI_CYCLE_COUNT structure [Battery Devices]","PBATTERY_WMI_CYCLE_COUNT","PBATTERY_WMI_CYCLE_COUNT structure pointer [Battery Devices]","batclass/BATTERY_WMI_CYCLE_COUNT","batclass/PBATTERY_WMI_CYCLE_COUNT","battery.battery_wmi_cycle_count"]
old-location: battery\battery_wmi_cycle_count.htm
tech.root: battery
ms.assetid: DFC94773-C198-4FC4-813C-0986ABA953A5
ms.date: 12/05/2018
ms.keywords: '*PBATTERY_WMI_CYCLE_COUNT, BATTERY_WMI_CYCLE_COUNT, BATTERY_WMI_CYCLE_COUNT structure [Battery Devices], PBATTERY_WMI_CYCLE_COUNT, PBATTERY_WMI_CYCLE_COUNT structure pointer [Battery Devices], batclass/BATTERY_WMI_CYCLE_COUNT, batclass/PBATTERY_WMI_CYCLE_COUNT, battery.battery_wmi_cycle_count'
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
targetos: Windows
req.typenames: BATTERY_WMI_CYCLE_COUNT, *PBATTERY_WMI_CYCLE_COUNT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _BATTERY_WMI_CYCLE_COUNT
 - batclass/_BATTERY_WMI_CYCLE_COUNT
 - PBATTERY_WMI_CYCLE_COUNT
 - batclass/PBATTERY_WMI_CYCLE_COUNT
 - BATTERY_WMI_CYCLE_COUNT
 - batclass/BATTERY_WMI_CYCLE_COUNT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Batclass.h
api_name:
 - BATTERY_WMI_CYCLE_COUNT
---

# BATTERY_WMI_CYCLE_COUNT structure


## -description

Defines information about number of charge cycles of a battery for use with the <a href="/windows/desktop/api/batclass/nf-batclass-batteryclassquerywmidatablock">BatteryClassQueryWmiDataBlock</a> function.

## -struct-fields

### -field Tag

A tag that identifies a specific battery.

### -field CycleCount

The number of charge/discharge cycles the battery has experienced, or zero if the battery does not support a cycle counter.

## -see-also

<a href="/windows/desktop/api/batclass/nf-batclass-batteryclassquerywmidatablock">BatteryClassQueryWmiDataBlock</a>