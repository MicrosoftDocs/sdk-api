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

# HrtfDirectivityCone structure


## -description


Describes a cone directivity.


## -struct-fields




### -field directivity

Descriptor for the cone pattern. The type parameter must be set to HrtfDirectivityType.Cone. 


### -field innerAngle

Angle, in radians, that defines the inner cone. Must be between 0 and 2 * pi.


### -field outerAngle

Angle, in radians, that defines the outer cone. Must be between 0 and 2 * pi.


## -remarks



Attenuation is 0 inside the inner cone.   Attenuation is linearly interpolated between the inner cone, which is defined by <i>innerAngle</i>, and the outer cone, which is defined by <i>outerAngle.</i>




## -see-also




<a href="https://msdn.microsoft.com/830DB9FC-B2D0-46E5-B0C1-0BBC94D37050">HrtfDirectivity</a>



<a href="https://msdn.microsoft.com/0705BB4C-01FE-434A-889B-F0D24D06DEF3">HrtfDirectivityCardioid</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn927277">Structures</a>
 

 

