---
UID: NF:directxmath.XMColorAdjustSaturation
title: XMColorAdjustSaturation function
author: windows-sdk-content
description: Adjusts the saturation value of a color.
old-location: dxmath\xmcoloradjustsaturation.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.color.XMColorAdjustSaturation(XMVECTOR,float)
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: Use DirectX..XMColorAdjustSaturation, XMColorAdjustSaturation, XMColorAdjustSaturation method [DirectX Math Support APIs], dxmath.xmcoloradjustsaturation
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
 - XMColorAdjustSaturation
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- XMColorAdjustSaturation
: 
---

# XMColorAdjustSaturation function


## -description


Adjusts the saturation value of a color.


## -parameters




### -param C [in]

<b>XMVECTOR</b> describing the color. Each of the components of <i>C</i> should be in the range 0.0f to 1.0f.


### -param Saturation [in]

Saturation value. This parameter linearly interpolates between the color converted to gray-scale and the original color,
        <i>C</i>. If <i>Saturation</i> is 0.0f, the function returns the gray-scale color. If
        <i>Saturation</i> is 1.0f, the function returns the original color.


## -returns



Returns an <b>XMVECTOR</b> describing the color resulting from the saturation adjustment.




## -remarks



The following pseudocode demonstrates the operation of the function.

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>XMVector colorOut;

// Approximate values for each component's contribution to luminance.
// Based upon the NTSC standard described in ITU-R Recommendation BT.709.
float Luminance = 0.2125f * C.x + 0.7154f * C.y + 0.0721f * C.z;

colorOut.x = (C.x - Luminance) * Saturation + Luminance;
colorOut.y = (C.y - Luminance) * Saturation + Luminance;
colorOut.z = (C.z - Luminance) * Saturation + Luminance;
colorOut.w = C.w;

return colorOut;</pre>
</td>
</tr>
</table></span></div>
<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/857e2aed-d082-d990-1c67-e22ce3d07310">DirectXMath Library Color Functions</a>
 

 

