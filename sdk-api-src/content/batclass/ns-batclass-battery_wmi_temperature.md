---
UID: NS:batclass._BATTERY_WMI_TEMPERATURE
title: BATTERY_WMI_TEMPERATURE (batclass.h)
description: Defines information about temperature of the battery for use with the BatteryClassQueryWmiDataBlock function.
helpviewer_keywords: ["*PBATTERY_WMI_TEMPERATURE","BATTERY_WMI_TEMPERATURE","BATTERY_WMI_TEMPERATURE structure [Battery Devices]","PBATTERY_WMI_TEMPERATURE","PBATTERY_WMI_TEMPERATURE structure pointer [Battery Devices]","batclass/BATTERY_WMI_TEMPERATURE","batclass/PBATTERY_WMI_TEMPERATURE","battery.battery_wmi_temperature"]
old-location: battery\battery_wmi_temperature.htm
tech.root: battery
ms.assetid: 341DA703-EB96-4680-AFB8-68043988AF56
ms.date: 12/05/2018
ms.keywords: '*PBATTERY_WMI_TEMPERATURE, BATTERY_WMI_TEMPERATURE, BATTERY_WMI_TEMPERATURE structure [Battery Devices], PBATTERY_WMI_TEMPERATURE, PBATTERY_WMI_TEMPERATURE structure pointer [Battery Devices], batclass/BATTERY_WMI_TEMPERATURE, batclass/PBATTERY_WMI_TEMPERATURE, battery.battery_wmi_temperature'
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
req.typenames: BATTERY_WMI_TEMPERATURE, *PBATTERY_WMI_TEMPERATURE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _BATTERY_WMI_TEMPERATURE
 - batclass/_BATTERY_WMI_TEMPERATURE
 - PBATTERY_WMI_TEMPERATURE
 - batclass/PBATTERY_WMI_TEMPERATURE
 - BATTERY_WMI_TEMPERATURE
 - batclass/BATTERY_WMI_TEMPERATURE
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
 - BATTERY_WMI_TEMPERATURE
---

# BATTERY_WMI_TEMPERATURE structure


## -description

 Defines information about temperature of the battery for use with the <a href="/windows/desktop/api/batclass/nf-batclass-batteryclassquerywmidatablock">BatteryClassQueryWmiDataBlock</a> function.

## -struct-fields

### -field Tag

A tag that identifies a specific battery.

### -field Temperature

The temperature.

## -see-also

<a href="/windows/desktop/api/batclass/nf-batclass-batteryclassquerywmidatablock">BatteryClassQueryWmiDataBlock</a>