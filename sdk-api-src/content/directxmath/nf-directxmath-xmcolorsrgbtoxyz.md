---
UID: NF:directxmath.XMColorSRGBToXYZ
title: XMColorSRGBToXYZ function
author: windows-sdk-content
description: Converts SRGB color values to XYZ color values.
old-location: dxmath\xmcolorsrgbtoxyz.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.color.XMColorSRGBToXYZ(XMVECTOR)
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: Use DirectX..XMColorSRGBToXYZ, XMColorSRGBToXYZ, XMColorSRGBToXYZ method [DirectX Math Support APIs], dxmath.xmcolorsrgbtoxyz
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
 - XMColorSRGBToXYZ
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- XMColorSRGBToXYZ
: 
---

# XMColorSRGBToXYZ function


## -description


Converts SRGB color values to XYZ color values.


## -parameters




### -param srgb [in]

Color value to convert. X element is Red, Y element is Green, Z element is Blue, and W element is Alpha. Each has a range of 0.0 to 1.0 and is in the linear sRGB colorspace.


## -returns



 Returns the converted color value with the trisimulus values of X, Y, and Z in the corresponding element, and the W element with Alpha (a copy of rgb.w). Each has a range of 0.0 to 1.0.




## -remarks



 Uses the CIE XYZ colorspace.

The sRGB linear color space is defined as IEC 61966-2-1:1999.

<div class="alert"><b>Note</b>  <code>XMColorSRGBToXYZ</code> is new for DirectXMath and is not available for XNAMath 2.x.</div>
<div> </div>
<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/857e2aed-d082-d990-1c67-e22ce3d07310">DirectXMath Library Color Functions</a>



<a href="https://msdn.microsoft.com/77d0d63b-bd99-46c4-8687-18297fe252aa">XMColorXYZToSRGB</a>
 

 

