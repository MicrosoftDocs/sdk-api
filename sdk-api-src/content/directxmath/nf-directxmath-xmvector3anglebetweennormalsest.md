---
UID: NF:directxmath.XMVector3AngleBetweenNormalsEst
title: XMVector3AngleBetweenNormalsEst function (directxmath.h)
description: Estimates the radian angle between two normalized 3D vectors.helpviewer_keywords: ["Use DirectX..XMVector3AngleBetweenNormalsEst","XMVector3AngleBetweenNormalsEst","XMVector3AngleBetweenNormalsEst method [DirectX Math Support APIs]","dxmath.xmvector3anglebetweennormalsest"]
old-location: dxmath\xmvector3anglebetweennormalsest.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.geometric.XMVector3AngleBetweenNormalsEst(XMVECTOR,XMVECTOR)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMVector3AngleBetweenNormalsEst, XMVector3AngleBetweenNormalsEst, XMVector3AngleBetweenNormalsEst method [DirectX Math Support APIs], dxmath.xmvector3anglebetweennormalsest
f1_keywords:
- directxmath/XMVector3AngleBetweenNormalsEst
dev_langs:
- c++
req.header: directxmath.h
req.include-header: DirectXMath.h
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
- directxmathvector.inl
api_name:
- XMVector3AngleBetweenNormalsEst
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# XMVector3AngleBetweenNormalsEst function


## -description


Estimates the radian angle between two normalized 3D vectors.


## -parameters




### -param N1 [in]

Normalized 3D vector.


### -param N2 [in]

Normalized 3D vector.


## -returns



Returns a vector. The estimate of the radian angle (between <i>N1</i> and <i>N2</i>) is replicated to each of the components.




## -remarks



<code>Est</code> functions offer increased performance at the expense of reduced accuracy.
    <code>Est</code> functions are appropriate for non-critical calculations where accuracy can be sacrificed for speed.
    The exact amount of lost accuracy and speed increase are platform dependent.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/dxmath/ovw-xnamath-reference-functions-vector3-geometric">DirectXMath Library 3D Vector Geometric Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/directxmath/nf-directxmath-xmvector3anglebetweennormals">XMVector3AngleBetweenNormals</a>
 

 

