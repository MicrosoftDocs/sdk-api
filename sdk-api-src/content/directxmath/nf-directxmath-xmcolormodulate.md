---
UID: NF:directxmath.XMColorModulate
title: XMColorModulate function
author: windows-sdk-content
description: Blends two colors by multiplying corresponding components together.
old-location: dxmath\xmcolormodulate.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.color.XMColorModulate(XMVECTOR,XMVECTOR)
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: Use DirectX..XMColorModulate, XMColorModulate, XMColorModulate method [DirectX Math Support APIs], dxmath.xmcolormodulate
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
 - XMColorModulate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- XMColorModulate
: 
---

# XMColorModulate function


## -description


Blends two colors by multiplying corresponding components together.


## -parameters




### -param C1 [in]

<b>XMVECTOR</b> describing the first color.


### -param C2 [in]

<b>XMVECTOR</b> describing the second color.


## -returns



Returns an <b>XMVECTOR</b> describing the color resulting from the modulation.




## -remarks



The following pseudocode demonstrates the operation of the function.

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>XMVECTOR colorOut;

colorOut.x = C1.x * C2.x;
colorOut.y = C1.y * C2.y;
colorOut.z = C1.z * C2.z;
colorOut.w = C1.w * C2.w;

return colorOut;</pre>
</td>
</tr>
</table></span></div>
<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/857e2aed-d082-d990-1c67-e22ce3d07310">DirectXMath Library Color Functions</a>
 

 

