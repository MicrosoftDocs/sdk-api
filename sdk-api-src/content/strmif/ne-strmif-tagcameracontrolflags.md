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

# tagCameraControlFlags enumeration


## -description



The <b>CameraControlFlags</b> enumeration defines whether a camera setting is controlled manually or automatically.




## -enum-fields




### -field CameraControl_Flags_Auto


            The setting is controlled automatically.
          


### -field CameraControl_Flags_Manual


            The setting is controlled manually.
          


## -remarks



In addition, the following flags are defined in Ksmedia.h:

<table>
<tr>
<th>Flag</th>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td><b>KSPROPERTY_CAMERACONTROL_FLAGS_AUTO</b></td>
<td>0X0001L</td>
<td>Equivalent to CameraControl_Flags_Auto.</td>
</tr>
<tr>
<td><b>KSPROPERTY_CAMERACONTROL_FLAGS_MANUAL</b></td>
<td>0X0002L</td>
<td>Equivalent to CameraControl_Flags_Manual.</td>
</tr>
<tr>
<td><b>KSPROPERTY_CAMERACONTROL_FLAGS_ABSOLUTE</b></td>
<td>0X0000L</td>
<td>The camera supports absolute units for this setting.</td>
</tr>
<tr>
<td><b>KSPROPERTY_CAMERACONTROL_FLAGS_RELATIVE</b></td>
<td>0X0010L</td>
<td>The camera supports relative controls for this setting. A relative control is divided into a number of steps with no defined units. The absolute size of each step depends on the camera model.</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/74467006-b077-49c0-8573-f939ac3d3444">DirectShow Enumerated Types</a>



<a href="https://msdn.microsoft.com/22bc35f1-76d4-4881-91d1-72f05c24561d">IAMCameraControl Interface</a>
 

 

