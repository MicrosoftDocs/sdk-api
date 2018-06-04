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

# D2D1_EXTEND_MODE enumeration


## -description


Specifies how a brush paints areas outside of its normal content area.


## -enum-fields




### -field D2D1_EXTEND_MODE_CLAMP

Repeat the edge pixels of the brush's content for all regions outside the normal content area.


### -field D2D1_EXTEND_MODE_WRAP

Repeat the brush's content.


### -field D2D1_EXTEND_MODE_MIRROR

 The same as D2D1_EXTEND_MODE_WRAP, except that alternate tiles of the brush's content are flipped. (The brush's normal content is drawn untransformed.)


### -field D2D1_EXTEND_MODE_FORCE_DWORD




## -remarks



For an <a href="https://msdn.microsoft.com/22b14ffa-14cb-4e4d-bf80-7d81e4ae9ee4">ID2D1BitmapBrush</a>, the brush's content is the brush's bitmap. For an <a href="https://msdn.microsoft.com/bbb5e36a-d13d-448e-8686-d14ee99b1ccb">ID2D1LinearGradientBrush</a>, the brush's content area is the gradient axis. For an <a href="https://msdn.microsoft.com/21ed2286-e4df-4b77-ba31-e5d5927e16f5">ID2D1RadialGradientBrush</a>, the brush's content is the area within the gradient ellipse.  




## -see-also




<a href="https://msdn.microsoft.com/bb20c9ea-a2b1-4fa5-a0e3-b788fe493993">ID2D1BitmapBrush::SetExtendModeX</a>



<a href="https://msdn.microsoft.com/6039ad41-e4b4-41e2-a4b1-31ad93ba88fd">ID2D1BitmapBrush::SetExtendModeY</a>



<a href="https://msdn.microsoft.com/c5f3facf-f1fe-4a47-b283-c0c859d8bc03">ID2D1RenderTarget::CreateGradientStopCollection</a>
 

 

