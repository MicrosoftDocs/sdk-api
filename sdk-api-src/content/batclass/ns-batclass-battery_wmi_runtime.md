---
UID: NS:batclass._BATTERY_WMI_RUNTIME
title: BATTERY_WMI_RUNTIME (batclass.h)
author: windows-sdk-content
description: Defines information about the estimated runtime of a battery for use with the BatteryClassQueryWmiDataBlock function.
old-location: battery\battery_wmi_runtime.htm
tech.root: battery
ms.assetid: B6351A10-581C-42F1-A8AD-D33D6F633466
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PBATTERY_WMI_RUNTIME, BATTERY_WMI_RUNTIME, BATTERY_WMI_RUNTIME structure [Battery Devices], PBATTERY_WMI_RUNTIME, PBATTERY_WMI_RUNTIME structure pointer [Battery Devices], batclass/BATTERY_WMI_RUNTIME, batclass/PBATTERY_WMI_RUNTIME, battery.battery_wmi_runtime"
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
 - BATTERY_WMI_RUNTIME
product: Windows
targetos: Windows
req.typenames: BATTERY_WMI_RUNTIME, *PBATTERY_WMI_RUNTIME
req.redist: 
---

# BATTERY_WMI_RUNTIME structure


## -description


Defines information about the estimated runtime of a battery for use with the <a href="https://msdn.microsoft.com/2a5c4c14-fc80-4a0a-b447-6fe33ff1d42f">BatteryClassQueryWmiDataBlock</a> function.


## -struct-fields




### -field Tag

A tag that identifies a specific battery.


### -field EstimatedRuntime

Specifies the estimated battery run time, in seconds.

This calculation may be based on the present rate of drain and not be very accurate on some battery systems. The estimate may vary widely depending on present power usage, which could be affected by disk activity and other factors. BATTERY_UNKNOWN_TIME is returned when no estimate is available.


## -see-also




<a href="https://msdn.microsoft.com/2a5c4c14-fc80-4a0a-b447-6fe33ff1d42f">BatteryClassQueryWmiDataBlock</a>
 

 

