---
UID: NF:directxmath.XMColorHSVToRGB
title: XMColorHSVToRGB function (directxmath.h)
description: Converts HSV color values to RGB color values.helpviewer_keywords: ["Use DirectX..XMColorHSVToRGB","XMColorHSVToRGB","XMColorHSVToRGB method [DirectX Math Support APIs]","dxmath.xmcolorhsvtorgb"]
old-location: dxmath\xmcolorhsvtorgb.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.color.XMColorHSVToRGB(XMVECTOR)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMColorHSVToRGB, XMColorHSVToRGB, XMColorHSVToRGB method [DirectX Math Support APIs], dxmath.xmcolorhsvtorgb
f1_keywords:
- directxmath/XMColorHSVToRGB
dev_langs:
- c++
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
- XMColorHSVToRGB
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# XMColorHSVToRGB function


## -description


Converts HSV color values to RGB color values.


## -parameters




### -param hsv [in]

 Color value to convert. The X element is Hue (H), the Y element is Saturation (S), the Z element is Value (V), and the W element is Alpha. Each has a range of 0.0 to 1.0.


## -returns



Returns the converted color value. X element is Red, Y element is Green, Z element is Blue, and W element is Alpha (a copy of hsv.w) . Each has a range of 0.0 to 1.0.




## -remarks



<div class="alert"><b>Note</b>  <code>XMColorHSVToRGB</code> is new for DirectXMath and is not available for XNAMath 2.x.</div>
<div> </div>
<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/dxmath/ovw-xnamath-reference-functions-color">DirectXMath Library Color Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/directxmath/nf-directxmath-xmcolorrgbtohsv">XMColorRGBToHSV</a>
 

 

