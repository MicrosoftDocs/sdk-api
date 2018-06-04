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

# _BATTERY_WMI_FULL_CHARGED_CAPACITY structure


## -description


Defines information about the capacity of a battery for use with the <a href="https://msdn.microsoft.com/library/windows/hardware/ff536268">BatteryClassQueryWmiDataBlock</a>)


## -struct-fields




### -field Tag

A tag that identifies a specific battery.


### -field FullChargedCapacity

The  current fully charged capacity, measured for example in milliwatt-hours, of a battery. If BATTERY_CAPACITY_RELATIVE is set, the units are undefined. For more information see the <a href="https://msdn.microsoft.com/library/windows/hardware/ff536283">BATTERY_INFORMATION</a>.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff536268">BatteryClassQueryWmiDataBlock</a>
 

 

