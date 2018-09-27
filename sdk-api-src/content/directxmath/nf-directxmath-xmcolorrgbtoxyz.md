---
UID: NF:directxmath.XMColorRGBToXYZ
title: XMColorRGBToXYZ function
author: windows-sdk-content
description: Converts RGB color values to XYZ color values.
old-location: dxmath\xmcolorrgbtoxyz.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.color.XMColorRGBToXYZ(XMVECTOR)
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: Use DirectX..XMColorRGBToXYZ, XMColorRGBToXYZ, XMColorRGBToXYZ method [DirectX Math Support APIs], dxmath.xmcolorrgbtoxyz
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
 - XMColorRGBToXYZ
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# XMColorRGBToXYZ function


## -description


Converts RGB color values to XYZ color values.


## -parameters




### -param rgb [in]

Color value to convert. X element is Red, Y element is Green, Z element is Blue, and W element is Alpha. Each has a range of 0.0 to 1.0.


## -returns



Returns the converted color value with the trisimulus values of X, Y, and Z in the corresponding element, and the W element with Alpha (a copy of rgb.w). Each has a range of 0.0 to 1.0.




## -remarks



Uses the CIE XYZ colorspace.

<div class="alert"><b>Note</b>  <code>XMColorRGBToXYZ</code> is new for DirectXMath and is not available for XNAMath 2.x.</div>
<div> </div>
<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/857e2aed-d082-d990-1c67-e22ce3d07310">DirectXMath Library Color Functions</a>



<a href="https://msdn.microsoft.com/748485d7-1b40-4f4d-ad98-5082360bc84c">XMColorXYZToRGB</a>
 

 

