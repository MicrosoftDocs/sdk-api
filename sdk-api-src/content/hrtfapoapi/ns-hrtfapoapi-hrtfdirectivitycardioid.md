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

# HrtfDirectivityCardioid structure


## -description


Describes a cardioid directivity pattern. 


## -struct-fields




### -field directivity

Descriptor for the cardioid pattern. The type parameter must be set to HrtfDirectivityType.Cardioid.


### -field order

Controls the shape of the cardioid. The higher order the shape, the narrower it is. Must be greater than 0 and less than or equal to 32.


## -see-also




<a href="https://msdn.microsoft.com/830DB9FC-B2D0-46E5-B0C1-0BBC94D37050">HrtfDirectivity</a>



<a href="https://msdn.microsoft.com/88679E17-285A-41C1-87A5-C37AF66F327F">HrtfDirectivityCone</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn927277">Structures</a>
 

 

