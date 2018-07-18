---
UID: NE:strmif.tagCameraControlFlags
title: tagCameraControlFlags
author: windows-sdk-content
description: The CameraControlFlags enumeration defines whether a camera setting is controlled manually or automatically.
old-location: dshow\cameracontrolflags.htm
old-project: DirectShow
ms.assetid: 806322e7-9a70-4dc1-8b10-2479fb3ec935
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: CameraControlFlags, CameraControlFlags enumeration [DirectShow], CameraControlFlagsEnumeration, CameraControl_Flags_Auto, CameraControl_Flags_Manual, dshow.cameracontrolflags, strmif/CameraControlFlags, strmif/CameraControl_Flags_Auto, strmif/CameraControl_Flags_Manual, tagCameraControlFlags
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
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
tech.root: 
req.typenames: CameraControlFlags
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - strmif.h
api_name:
 - CameraControlFlags
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Outlook Express 6.0
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
 

 

