---
UID: NF:directxmath.XMMatrixOrthographicRH
title: XMMatrixOrthographicRH function (directxmath.h)
description: Builds an orthogonal projection matrix for a right-handed coordinate system.
old-location: dxmath\xmmatrixorthographicrh.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.matrix.XMMatrixOrthographicRH(float,float,float,float)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMMatrixOrthographicRH, XMMatrixOrthographicRH, XMMatrixOrthographicRH method [DirectX Math Support APIs], dxmath.xmmatrixorthographicrh
ms.topic: function
f1_keywords:
- directxmath/XMMatrixOrthographicRH
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
- XMMatrixOrthographicRH
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# XMMatrixOrthographicRH function


## -description


Builds an orthogonal projection matrix for a right-handed coordinate system.


## -parameters




### -param ViewWidth [in]

Width of the frustum at the near clipping plane.


### -param ViewHeight [in]

Height of the frustum at the near clipping plane.


### -param NearZ [in]

Distance to the near clipping plane. 


### -param FarZ [in]

Distance to the far clipping plane.


## -returns



Returns the orthogonal projection matrix.




## -remarks



All the parameters of
   <b>XMMatrixOrthographicRH</b> are distances
   in camera space.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/dxmath/ovw-xnamath-reference-functions-matrix">DirectXMath Library Matrix Functions</a>



<a href="https://docs.microsoft.com/en-us/windows/desktop/api/directxmath/nf-directxmath-xmmatrixorthographiclh">XMMatrixOrthographicLH</a>
 

 

