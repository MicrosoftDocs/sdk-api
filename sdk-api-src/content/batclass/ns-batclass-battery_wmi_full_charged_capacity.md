---
UID: NS:batclass._BATTERY_WMI_FULL_CHARGED_CAPACITY
title: BATTERY_WMI_FULL_CHARGED_CAPACITY (batclass.h)
description: Defines information about the capacity of a battery for use with the BatteryClassQueryWmiDataBlock).
helpviewer_keywords: ["*PBATTERY_WMI_FULL_CHARGED_CAPACITY","BATTERY_WMI_FULL_CHARGED_CAPACITY","BATTERY_WMI_FULL_CHARGED_CAPACITY structure [Battery Devices]","PBATTERY_WMI_FULL_CHARGED_CAPACITY","PBATTERY_WMI_FULL_CHARGED_CAPACITY structure pointer [Battery Devices]","batclass/BATTERY_WMI_FULL_CHARGED_CAPACITY","batclass/PBATTERY_WMI_FULL_CHARGED_CAPACITY","battery.battery_wmi_full_charged_capacity"]
old-location: battery\battery_wmi_full_charged_capacity.htm
tech.root: battery
ms.assetid: BE01DF36-71A8-464A-977B-499325DDB37E
ms.date: 12/05/2018
ms.keywords: '*PBATTERY_WMI_FULL_CHARGED_CAPACITY, BATTERY_WMI_FULL_CHARGED_CAPACITY, BATTERY_WMI_FULL_CHARGED_CAPACITY structure [Battery Devices], PBATTERY_WMI_FULL_CHARGED_CAPACITY, PBATTERY_WMI_FULL_CHARGED_CAPACITY structure pointer [Battery Devices], batclass/BATTERY_WMI_FULL_CHARGED_CAPACITY, batclass/PBATTERY_WMI_FULL_CHARGED_CAPACITY, battery.battery_wmi_full_charged_capacity'
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
req.typenames: BATTERY_WMI_FULL_CHARGED_CAPACITY, *PBATTERY_WMI_FULL_CHARGED_CAPACITY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _BATTERY_WMI_FULL_CHARGED_CAPACITY
 - batclass/_BATTERY_WMI_FULL_CHARGED_CAPACITY
 - PBATTERY_WMI_FULL_CHARGED_CAPACITY
 - batclass/PBATTERY_WMI_FULL_CHARGED_CAPACITY
 - BATTERY_WMI_FULL_CHARGED_CAPACITY
 - batclass/BATTERY_WMI_FULL_CHARGED_CAPACITY
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
 - BATTERY_WMI_FULL_CHARGED_CAPACITY
---

# BATTERY_WMI_FULL_CHARGED_CAPACITY structure


## -description

Defines information about the capacity of a battery for use with the <a href="/windows/desktop/api/batclass/nf-batclass-batteryclassquerywmidatablock">BatteryClassQueryWmiDataBlock</a>)

## -struct-fields

### -field Tag

A tag that identifies a specific battery.

### -field FullChargedCapacity

The  current fully charged capacity, measured for example in milliwatt-hours, of a battery. If BATTERY_CAPACITY_RELATIVE is set, the units are undefined. For more information see the <a href="/previous-versions/ff536283(v=vs.85)">BATTERY_INFORMATION</a>.

## -see-also

<a href="/windows/desktop/api/batclass/nf-batclass-batteryclassquerywmidatablock">BatteryClassQueryWmiDataBlock</a>