---
UID: NF:directxmath.XMMatrixLookAtRH
title: XMMatrixLookAtRH function (directxmath.h)
description: Builds a view matrix for a right-handed coordinate system using a camera position, an up direction, and a focal point.helpviewer_keywords: ["Use DirectX..XMMatrixLookAtRH","XMMatrixLookAtRH","XMMatrixLookAtRH method [DirectX Math Support APIs]","dxmath.xmmatrixlookatrh"]
old-location: dxmath\xmmatrixlookatrh.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.matrix.XMMatrixLookAtRH(XMVECTOR,XMVECTOR,XMVECTOR)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMMatrixLookAtRH, XMMatrixLookAtRH, XMMatrixLookAtRH method [DirectX Math Support APIs], dxmath.xmmatrixlookatrh
f1_keywords:
- directxmath/XMMatrixLookAtRH
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
- XMMatrixLookAtRH
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# XMMatrixLookAtRH function


## -description


Builds a view matrix for a right-handed coordinate system using a camera position, an up direction, and a focal point.


## -parameters




### -param EyePosition [in]

Position of the camera.


### -param FocusPosition [in]

Position of the focal point.


### -param UpDirection [in]

Up direction of the camera, typically &lt; 0.0f, 1.0f, 0.0f &gt;.


## -returns



Returns a view matrix that transforms a point from world space into view space.




## -remarks



<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/dxmath/ovw-xnamath-reference-functions-matrix">DirectXMath Library Matrix Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/directxmath/nf-directxmath-xmmatrixlookatlh">XMMatrixLookAtLH</a>
 

 

