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

# DIOBJECTCALIBRATION structure


## -description


The DIOBJECTCALIBRATION structure describes the information contained in the "Calibration" value of the registry key for each axis on a device.


## -struct-fields




### -field lMin

Specifies the logical value for the axis minimum position.


### -field lCenter

Specifies the logical value for the axis center position.


### -field lMax

Specifies the logical value for the axis maximum position.


## -remarks



If the "Calibration" value is absent, then the calibration information is taken from the joystick <a href="https://msdn.microsoft.com/library/windows/hardware/ff542256">JOYREGHWVALUES</a> configuration structure.

Only HID joysticks have a "Calibration" value.



