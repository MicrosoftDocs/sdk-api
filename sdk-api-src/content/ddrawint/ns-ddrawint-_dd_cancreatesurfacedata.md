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

# _DD_CANCREATESURFACEDATA structure


## -description


The DD_CANCREATESURFACEDATA structure contains information necessary to indicate whether a surface--in the case of <a href="https://msdn.microsoft.com/94aace9f-0927-4b33-a9ea-79c27d5edea9">CanCreateD3DBuffer</a>, a buffer--can be created.


## -struct-fields




### -field lpDD

Points to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff550586">DD_DIRECTDRAW_GLOBAL</a> structure that describes the driver's device. 


### -field lpDDSurfaceDesc

Points to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff550339">DDSURFACEDESC</a> structure that contains a description of the surface or buffer to be created. See the Remarks section for additional information about this member.


### -field bIsDifferentPixelFormat

Indicates whether the pixel format of the surface to be created differs from that of the primary surface. For the <a href="https://msdn.microsoft.com/94aace9f-0927-4b33-a9ea-79c27d5edea9">CanCreateD3DBuffer</a> D3DBuffer callback, this member is always set to <b>FALSE</b> because the driver is attempting to create a buffer that contains vertex data or commands, rather than pixel data.


### -field ddRVal

Specifies the location in which the driver writes the return value of either the <a href="https://msdn.microsoft.com/015b94d7-427f-401d-b348-d4e9ec5cfe5d">DdCanCreateSurface</a> or <a href="https://msdn.microsoft.com/94aace9f-0927-4b33-a9ea-79c27d5edea9">CanCreateD3DBuffer</a> callback. A return code of DD_OK indicates success. For more information, see <a href="https://msdn.microsoft.com/da4cc7d7-6826-48aa-96c6-004e31fc3e3e">Return Values for DirectDraw</a>.


### -field CanCreateSurface

Used by the Microsoft DirectDraw API and should not be filled in by the driver.


## -remarks



The DirectDraw surface description pointed to by the <b>lpDDSurfaceDesc</b> member is actually a <a href="https://msdn.microsoft.com/library/windows/hardware/ff550340">DDSURFACEDESC2</a> structure (rather than a DDSURFACEDESC structure) for DirectDraw 6.0 and later runtimes. Therefore, if you need information at surface-creation time from those members that are in the DDSURFACEDESC2 structure but not in the DDSURFACEDESC structure, you can simply cast the pointer to a DDSURFACEDESC structure to a pointer to a DDSURFACEDESC2 structure prior to use. The following example shows how the value of <b>dwTextureStage</b> (a member of the DDSURFACEDESC2 structure, but not also of the DDSURFACEDESC structure) can be obtained from a pointer to a DDSURFACEDESC structure.

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>DDSURFACEDESC2* pddsd = (DDSURFACEDESC2*)pccsd-&gt;lpDDSurfaceDesc;
DWORD dwStage = pddsd-&gt;dwTextureStage;</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/94aace9f-0927-4b33-a9ea-79c27d5edea9">CanCreateD3DBuffer</a>



<a href="https://msdn.microsoft.com/015b94d7-427f-401d-b348-d4e9ec5cfe5d">DdCanCreateSurface</a>
 

 

