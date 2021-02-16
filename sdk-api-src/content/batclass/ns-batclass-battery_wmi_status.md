---
UID: NS:batclass._BATTERY_WMI_STATUS
title: BATTERY_WMI_STATUS (batclass.h)
description: Defines battery status information.
helpviewer_keywords: ["*PBATTERY_WMI_STATUS","BATTERY_WMI_STATUS","BATTERY_WMI_STATUS structure [Battery Devices]","PBATTERY_WMI_STATUS","PBATTERY_WMI_STATUS structure pointer [Battery Devices]","batclass/BATTERY_WMI_STATUS","batclass/PBATTERY_WMI_STATUS","battery.battery_wmi_status"]
old-location: battery\battery_wmi_status.htm
tech.root: battery
ms.assetid: BE3FB7CA-928D-4A2E-A11D-20E9D3F8841E
ms.date: 12/05/2018
ms.keywords: '*PBATTERY_WMI_STATUS, BATTERY_WMI_STATUS, BATTERY_WMI_STATUS structure [Battery Devices], PBATTERY_WMI_STATUS, PBATTERY_WMI_STATUS structure pointer [Battery Devices], batclass/BATTERY_WMI_STATUS, batclass/PBATTERY_WMI_STATUS, battery.battery_wmi_status'
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
req.typenames: BATTERY_WMI_STATUS, *PBATTERY_WMI_STATUS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _BATTERY_WMI_STATUS
 - batclass/_BATTERY_WMI_STATUS
 - PBATTERY_WMI_STATUS
 - batclass/PBATTERY_WMI_STATUS
 - BATTERY_WMI_STATUS
 - batclass/BATTERY_WMI_STATUS
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
 - BATTERY_WMI_STATUS
---

# BATTERY_WMI_STATUS structure


## -description

Defines battery status information.

## -struct-fields

### -field Tag

A tag that identifies a specific battery.

### -field RemainingCapacity

The remaining capacity of the battery.

### -field ChargeRate

The charge rate of the battery.

### -field DischargeRate

The discharge rate of the battery.

### -field Voltage

The voltage of the battery.

### -field PowerOnline

Whether there is power online.

### -field Charging

Whether the battery is charging.

### -field Discharging

Whether the battery is discharging.

### -field Critical

Whether the power level is critical.

