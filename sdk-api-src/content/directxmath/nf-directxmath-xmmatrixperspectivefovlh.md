---
UID: NF:directxmath.XMMatrixPerspectiveFovLH
title: XMMatrixPerspectiveFovLH function
author: windows-sdk-content
description: Builds a left-handed perspective projection matrix based on a field of view.
old-location: dxmath\xmmatrixperspectivefovlh.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.matrix.XMMatrixPerspectiveFovLH(float,float,float,float)
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: Use DirectX..XMMatrixPerspectiveFovLH, XMMatrixPerspectiveFovLH, XMMatrixPerspectiveFovLH method [DirectX Math Support APIs], dxmath.xmmatrixperspectivefovlh
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
 - XMMatrixPerspectiveFovLH
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# XMMatrixPerspectiveFovLH function


## -description


Builds a left-handed perspective projection matrix based on a field of view.


## -parameters




### -param FovAngleY [in]

Top-down field-of-view angle in radians.


### -param AspectRatio [in]

Aspect ratio of view-space X:Y.


### -param NearZ [in]

Distance to the near clipping plane. Must be greater than zero.


### -param FarZ [in]

Distance to the far clipping plane. Must be greater than zero.


## -returns



Returns the perspective projection matrix.




## -remarks



For typical usage, <i>NearZ</i> is less than  <i>FarZ</i>. However, if you flip these values so <i>FarZ</i> is less than  <i>NearZ</i>, the result is an inverted z buffer which can provide increased floating-point precision.  <i>NearZ</i> and <i>FarZ</i> cannot be the same value.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/d59d0dcc-deae-3f7e-55c5-0c5ff383343b">DirectXMath Library Matrix Functions</a>



<a href="https://msdn.microsoft.com/587168e0-de74-4e51-95bc-f9dd3388ef35">XMMatrixPerspectiveFovRH</a>
 

 

