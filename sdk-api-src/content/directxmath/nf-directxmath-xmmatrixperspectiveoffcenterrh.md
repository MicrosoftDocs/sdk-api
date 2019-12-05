---
UID: NF:directxmath.XMMatrixPerspectiveOffCenterRH
title: XMMatrixPerspectiveOffCenterRH function (directxmath.h)
description: Builds a custom version of a right-handed perspective projection matrix.
old-location: dxmath\xmmatrixperspectiveoffcenterrh.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.matrix.XMMatrixPerspectiveOffCenterRH(float,float,float,float,float,float)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMMatrixPerspectiveOffCenterRH, XMMatrixPerspectiveOffCenterRH, XMMatrixPerspectiveOffCenterRH method [DirectX Math Support APIs], dxmath.xmmatrixperspectiveoffcenterrh
ms.topic: function
f1_keywords:
- directxmath/XMMatrixPerspectiveOffCenterRH
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
- XMMatrixPerspectiveOffCenterRH
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# XMMatrixPerspectiveOffCenterRH function


## -description


Builds a custom version of a right-handed perspective projection matrix.


## -parameters




### -param ViewLeft [in]

The x-coordinate of the left side of the clipping frustum at the near clipping plane.


### -param ViewRight [in]

The x-coordinate of the right side of the clipping frustum at the near clipping plane.


### -param ViewBottom [in]

The y-coordinate of the bottom side of the clipping frustum at the near clipping plane.


### -param ViewTop [in]

The y-coordinate of the top side of the clipping frustum at the near clipping plane.


### -param NearZ [in]

Distance to the near clipping plane. Must be greater than zero.


### -param FarZ [in]

Distance to the far clipping plane. Must be greater than  zero.


## -returns



Returns the custom perspective projection matrix.




## -remarks



For typical usage, <i>NearZ</i> is less than  <i>FarZ</i>. However, if you flip these values so <i>FarZ</i> is less than  <i>NearZ</i>, the result is an inverted z buffer which can provide increased floating-point precision.  <i>NearZ</i> and <i>FarZ</i> cannot be the same value.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/dxmath/ovw-xnamath-reference-functions-matrix">DirectXMath Library Matrix Functions</a>



<a href="https://docs.microsoft.com/en-us/windows/desktop/api/directxmath/nf-directxmath-xmmatrixperspectiveoffcenterlh">XMMatrixPerspectiveOffCenterLH</a>
 

 

