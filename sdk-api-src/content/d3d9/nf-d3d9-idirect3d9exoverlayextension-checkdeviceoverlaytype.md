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

# IDirect3D9ExOverlayExtension::CheckDeviceOverlayType


## -description


Queries the overlay hardware capabilities of a Direct3D device.


## -parameters




### -param Adapter [in]

An ordinal number that denotes the display adapter. <b>D3DADAPTER_DEFAULT</b> is always the primary display adapter. 



### -param DevType [in]

Specifies the Direct3D device type as a member of the <b>D3DDEVTYPE</b> enumerated type. 


### -param OverlayWidth [in]

The width of the overlay to create, in pixels.


### -param OverlayHeight [in]

The height of the overlay to create, in pixels.


### -param OverlayFormat [in]

The surface format of the overlay.


### -param pDisplayMode [in]

A pointer to a <b>D3DDISPLAYMODEEX</b> structure that specifies the display mode that will be used. If this parameter is <b>NULL</b>, the current display mode is assumed.


### -param DisplayRotation [in]

Specifies the display rotation mode as a member of the <b>D3DDISPLAYROTATION</b> enumerated type.


### -param pOverlayCaps [out]

A pointer to a <a href="https://msdn.microsoft.com/4d9e031d-af01-4b8a-b90c-9d83b09c24da">D3DOVERLAYCAPS</a> structure. If the driver supports the overlay settings specified in the input parameters, the method fills this structure with the capabilities of the overlay hardware.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>D3DERR_INVALIDCALL</b></dt>
</dl>
</td>
<td width="60%">
Invalid parameter, or the device does not support hardware overlay.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>D3DERR_UNSUPPORTEDOVERLAY</b></dt>
</dl>
</td>
<td width="60%">
The device does not support overlay for the specified size or display mode.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>D3DERR_UNSUPPORTEDOVERLAYFORMAT</b></dt>
</dl>
</td>
<td width="60%">
The device does not support overlay for the specified surface format.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/fa9d5bf5-4c0f-471a-b639-d329b0cd89a4">Hardware Overlay Support</a>



<a href="https://msdn.microsoft.com/57591794-96d3-40e6-a4fb-3bb195fd1396">IDirect3D9ExOverlayExtension</a>
 

 

