---
UID: NF:directxmath.XMColorHSLToRGB
title: XMColorHSLToRGB function
author: windows-sdk-content
description: Converts HSL color values to RGB color values.
old-location: dxmath\xmcolorhsltorgb.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.color.XMColorHSLToRGB(XMVECTOR)
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: Use DirectX..XMColorHSLToRGB, XMColorHSLToRGB, XMColorHSLToRGB method [DirectX Math Support APIs], dxmath.xmcolorhsltorgb
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
 - XMColorHSLToRGB
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- XMColorHSLToRGB
: 
---

# XMColorHSLToRGB function


## -description


Converts HSL color values to RGB color values.


## -parameters




### -param hsl [in]

Color value to convert. The X element is Hue (H), the Y element is Saturation (S), the Z element is Luminance (L), 
        and the W element is Alpha. Each has a range of 0.0 to 1.0.


## -returns



Returns the converted color value. X element is Red, Y element is Green, Z element is Blue, and W element is Alpha (a copy of hsl.w) . Each has a range of 0.0 to 1.0.




## -remarks



<div class="alert"><b>Note</b>  <code>XMColorHSLToRGB</code> is new for DirectXMath and is not available for XNAMath 2.x.</div>
<div> </div>
<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/857e2aed-d082-d990-1c67-e22ce3d07310">DirectXMath Library Color Functions</a>



<a href="https://msdn.microsoft.com/d68d1d75-e5fb-4f65-837b-25a4c98e990d">XMColorRGBToHSL</a>
 

 

