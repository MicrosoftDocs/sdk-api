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

# tagCameraControlProperty enumeration


## -description



The <code>CameraControlProperty</code> enumeration specifies a setting on a camera.




## -enum-fields




### -field CameraControl_Pan

Specifies the camera's pan setting, in degrees. Values range from –180 to +180, with the default set to zero. Positive values are clockwise from the origin (the camera rotates clockwise when viewed from above), and negative values are counterclockwise from the origin.


### -field CameraControl_Tilt

Specifies the camera's tilt setting, in degrees. Values range from –180 to +180, with the default set to zero. Positive values point the imaging plane up, and negative values point the imaging plane down.


### -field CameraControl_Roll

Specifies the camera's roll setting, in degrees. Values range from –180 to +180, with the default set to zero. Positive values cause a clockwise rotation of the camera along the image-viewing axis, and negative values cause a counterclockwise rotation of the camera.


### -field CameraControl_Zoom

Specifies the camera's zoom setting, in millimeters. Values range from 10 to 600, and the default is specific to the device.


### -field CameraControl_Exposure

Specifies the exposure setting, in log base 2 seconds. In other words, for values less than zero, the exposure time is 1/2^n seconds, and for values zero or above, the exposure time is 2^n seconds. For example:

<table>
<tr>
<th>
                  Value
                </th>
<th>
                  Seconds
                </th>
</tr>
<tr>
<td>-3</td>
<td>1/8</td>
</tr>
<tr>
<td>-2</td>
<td>1/4</td>
</tr>
<tr>
<td>-1</td>
<td>1/2</td>
</tr>
<tr>
<td>0</td>
<td>1</td>
</tr>
<tr>
<td>1</td>
<td>2</td>
</tr>
<tr>
<td>2</td>
<td>4</td>
</tr>
</table>
 


### -field CameraControl_Iris

Specifies the camera's iris setting, in units of fₛₜₒₚ* 10.


### -field CameraControl_Focus

Specifies the camera's focus setting, as the distance to the optimally focused target, in millimeters. The range and default value are specific to the device.


## -remarks



For a given property, a particular device might implement only a subset of the listed range.




## -see-also




<a href="https://msdn.microsoft.com/74467006-b077-49c0-8573-f939ac3d3444">DirectShow Enumerated Types</a>



<a href="https://msdn.microsoft.com/22bc35f1-76d4-4881-91d1-72f05c24561d">IAMCameraControl Interface</a>
 

 

