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

# _BATTERY_WMI_CYCLE_COUNT structure


## -description


Defines information about number of charge cycles of a battery for use with the <a href="https://msdn.microsoft.com/library/windows/hardware/ff536268">BatteryClassQueryWmiDataBlock</a> function.


## -struct-fields




### -field Tag

A tag that identifies a specific battery.


### -field CycleCount

The number of charge/discharge cycles the battery has experienced, or zero if the battery does not support a cycle counter.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff536268">BatteryClassQueryWmiDataBlock</a>
 

 

