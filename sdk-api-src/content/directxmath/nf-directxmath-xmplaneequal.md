---
UID: NF:directxmath.XMPlaneEqual
title: XMPlaneEqual function
author: windows-sdk-content
description: Determines if two planes are equal.
old-location: dxmath\xmplaneequal.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.plane.XMPlaneEqual(XMVECTOR,XMVECTOR)
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: Use DirectX..XMPlaneEqual, XMPlaneEqual, XMPlaneEqual method [DirectX Math Support APIs], dxmath.xmplaneequal
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
 - XMPlaneEqual
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- XMPlaneEqual
: 
---

# XMPlaneEqual function


## -description


Determines if two planes are equal.


## -parameters




### -param P1 [in]

<b>XMVECTOR</b> describing the plane coefficients (A, B, C, D) for the plane equation <div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>return (P1.x == P2.x &amp;&amp; P1.y == P2.y &amp;&amp; P1.z == P2.z &amp;&amp; P1.w == P2.w);</pre>
</td>
</tr>
</table></span></div>.


### -param P2 [in]

<b>XMVECTOR</b> describing the plane coefficients (A, B, C, D) for the plane equation <code>Ax+By+Cz+D=0</code>.


## -returns



Returns true if the two planes are equal and false otherwise.




## -remarks



The following pseudocode demonstrates the operation of the function.

<code>Ax+By+Cz+D=0</code>

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/6505e72e-4af5-5db3-4fc0-f83fa77692b1">DirectXMath Library Plane Functions</a>
 

 

