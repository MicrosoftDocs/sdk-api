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

# TabletHardwareCapabilities enumeration


## -description



Specifies the hardware capabilities of the Tablet PC.




## -enum-fields




### -field THWC_Integrated

The digitizer is integrated with the display.


### -field THWC_CursorMustTouch

The cursor must be in physical contact with the device to report position.


### -field THWC_HardProximity

The device can generate in-air packets when the cursor is in the physical detection range (proximity) of the device.


### -field THWC_CursorsHavePhysicalIds

The device can uniquely identify the active cursor.


## -remarks



In C++, explicit casting is required when trying to set more than one flag at a time. A compilation error occurs if explicit casting is not used.

The value is 0 if the tablet device cannot provide this information.

This enumeration is a flag.




## -see-also




<a href="https://msdn.microsoft.com/886c1e7c-fec0-4294-aba1-8e0806c2d0ca">HardwareCapabilities Property</a>



<a href="https://msdn.microsoft.com/9a945740-b191-41f5-8b3d-49b7e2d1e463">IInkTablet Interface</a>
 

 

