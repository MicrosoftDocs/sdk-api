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

# X3DAUDIO_DISTANCE_CURVE structure


## -description


Defines an explicit piecewise curve made up of linear segments, directly defining DSP behavior with respect to normalized distance.


## -struct-fields




### -field pPoints


<a href="https://msdn.microsoft.com/29f8d152-b254-4b42-a985-d8412ea35037">X3DAUDIO_DISTANCE_CURVE_POINT</a> array. The array must have no duplicates and be sorted in ascending order with respect to distance.


### -field PointCount

Number of distance curve points. There must be two or more points since all curves must have at least two endpoints defining values at 0.0f and 1.0f normalized distance, respectively.


## -remarks



<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn927277">Structures</a>
 

 

