---
UID: NF:directxmath.XMColorRGBToSRGB
title: XMColorRGBToSRGB function
author: windows-sdk-content
description: Converts an RGB color vector to sRGB.
old-location: dxmath\_xmcolorrgbtosrgb.htm
tech.root: dxmath
ms.assetid: ADD40A97-6BE1-4EDA-BBBB-6B186694F3E6
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: Use DirectX..XMColorRGBToSRGB, XMColorRGBToSRGB, XMColorRGBToSRGB method [DirectX Math Support APIs], dxmath._xmcolorrgbtosrgb
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: directxmath.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: Use DirectX.
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DirectXMath.h
api_name:
 - XMColorRGBToSRGB
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- XMColorRGBToSRGB
: 
---

# XMColorRGBToSRGB function


## -description


Converts an RGB color vector to sRGB.


## -parameters




### -param rgb

The original RGB color vector.


## -returns



Returns an <b>XMVECTOR</b> describing the converted sRGBA color vector. The x element is red, the y element is green, the z element is blue, and the w element is the alpha value (which is a copy of rgb.w). Each element value has a range of 0.0 to 1.0 in the sRGB colorspace. 




## -see-also




<a href="https://msdn.microsoft.com/857e2aed-d082-d990-1c67-e22ce3d07310">DirectXMath Library Color Functions</a>



<a href="https://msdn.microsoft.com/A0F6AC87-AA83-4BF0-8259-577EABA72539">XMColorSRGBToRGB</a>
 

 

