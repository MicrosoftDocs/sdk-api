---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# _BATTERY_WMI_RUNTIME structure


## -description


Defines information about the estimated runtime of a battery for use with the <a href="https://msdn.microsoft.com/library/windows/hardware/ff536268">BatteryClassQueryWmiDataBlock</a> function.


## -struct-fields




### -field Tag

A tag that identifies a specific battery.


### -field EstimatedRuntime

Specifies the estimated battery run time, in seconds.

This calculation may be based on the present rate of drain and not be very accurate on some battery systems. The estimate may vary widely depending on present power usage, which could be affected by disk activity and other factors. BATTERY_UNKNOWN_TIME is returned when no estimate is available.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff536268">BatteryClassQueryWmiDataBlock</a>
 

 

