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

# MFVideoAlphaBitmap structure


## -description



Specifies a bitmap for the enhanced video renderer (EVR) to alpha-blend with the video.




## -struct-fields




### -field GetBitmapFromDC

If <b>TRUE</b>, the <b>hdc</b> member is used. Otherwise, the <b>pDDs</b> member is used.


### -field bitmap

A union that contains the following members.



#### pDDs

Pointer to the <b>IDirect3DSurface9</b> interface of a Direct3D surface that contains the bitmap. If <b>GetBitmapFromDC</b> is <b>TRUE</b>, this member is ignored.


### -field bitmap.hdc

Handle to the device context (DC) of a GDI bitmap. If <b>GetBitmapFromDC</b> is <b>FALSE</b>, this member is ignored.


### -field bitmap.pDDS

 


### -field params


<a href="https://msdn.microsoft.com/3a7f67fa-ca54-4b6f-9cfc-e8eba57f00ce">MFVideoAlphaBitmapParams</a> structure that specifies the parameters for the alpha-blending operation.


## -remarks



To specify a GDI bitmap, create a device context and call <b>SelectObject</b> to select the bitmap into the DC. Then set the <b>hdc</b> member of the structure equal to the handle to the DC and set the <b>GetBitmapFromDC</b> member to <b>TRUE</b>.




## -see-also




<a href="https://msdn.microsoft.com/1c985558-d25d-4f51-978a-58c05943dab9">Enhanced Video Renderer</a>



<a href="https://msdn.microsoft.com/a70e6734-bf49-4dea-8bf6-917b8465cc78">IMFVideoMixerBitmap::SetAlphaBitmap</a>



<a href="https://msdn.microsoft.com/39fdd724-13ca-48ab-8a55-93529d1da3b4">Media Foundation Structures</a>
 

 

