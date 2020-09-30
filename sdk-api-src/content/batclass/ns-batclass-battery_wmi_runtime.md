---
UID: NS:batclass._BATTERY_WMI_RUNTIME
title: BATTERY_WMI_RUNTIME (batclass.h)
description: Defines information about the estimated runtime of a battery for use with the BatteryClassQueryWmiDataBlock function.
helpviewer_keywords: ["*PBATTERY_WMI_RUNTIME","BATTERY_WMI_RUNTIME","BATTERY_WMI_RUNTIME structure [Battery Devices]","PBATTERY_WMI_RUNTIME","PBATTERY_WMI_RUNTIME structure pointer [Battery Devices]","batclass/BATTERY_WMI_RUNTIME","batclass/PBATTERY_WMI_RUNTIME","battery.battery_wmi_runtime"]
old-location: battery\battery_wmi_runtime.htm
tech.root: battery
ms.assetid: B6351A10-581C-42F1-A8AD-D33D6F633466
ms.date: 12/05/2018
ms.keywords: '*PBATTERY_WMI_RUNTIME, BATTERY_WMI_RUNTIME, BATTERY_WMI_RUNTIME structure [Battery Devices], PBATTERY_WMI_RUNTIME, PBATTERY_WMI_RUNTIME structure pointer [Battery Devices], batclass/BATTERY_WMI_RUNTIME, batclass/PBATTERY_WMI_RUNTIME, battery.battery_wmi_runtime'
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
req.typenames: BATTERY_WMI_RUNTIME, *PBATTERY_WMI_RUNTIME
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _BATTERY_WMI_RUNTIME
 - batclass/_BATTERY_WMI_RUNTIME
 - PBATTERY_WMI_RUNTIME
 - batclass/PBATTERY_WMI_RUNTIME
 - BATTERY_WMI_RUNTIME
 - batclass/BATTERY_WMI_RUNTIME
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
 - BATTERY_WMI_RUNTIME
---

# BATTERY_WMI_RUNTIME structure


## -description

Defines information about the estimated runtime of a battery for use with the <a href="/windows/desktop/api/batclass/nf-batclass-batteryclassquerywmidatablock">BatteryClassQueryWmiDataBlock</a> function.

## -struct-fields

### -field Tag

A tag that identifies a specific battery.

### -field EstimatedRuntime

Specifies the estimated battery run time, in seconds.

This calculation may be based on the present rate of drain and not be very accurate on some battery systems. The estimate may vary widely depending on present power usage, which could be affected by disk activity and other factors. BATTERY_UNKNOWN_TIME is returned when no estimate is available.

## -see-also

<a href="/windows/desktop/api/batclass/nf-batclass-batteryclassquerywmidatablock">BatteryClassQueryWmiDataBlock</a>