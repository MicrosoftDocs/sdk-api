---
UID: NF:directxmath.XMVectorCatmullRomV
title: XMVectorCatmullRomV function (directxmath.h)
description: Performs a Catmull-Rom interpolation, using the specified position vectors. (XMVectorCatmullRomV)
helpviewer_keywords: ["Use DirectX..XMVectorCatmullRomV","XMVectorCatmullRomV","XMVectorCatmullRomV method [DirectX Math Support APIs]","dxmath.xmvectorcatmullromv"]
old-location: dxmath\xmvectorcatmullromv.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.geometric.XMVectorCatmullRomV(XMVECTOR,XMVECTOR,XMVECTOR,XMVECTOR,XMVECTOR)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMVectorCatmullRomV, XMVectorCatmullRomV, XMVectorCatmullRomV method [DirectX Math Support APIs], dxmath.xmvectorcatmullromv
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - XMVectorCatmullRomV
 - directxmath/XMVectorCatmullRomV
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - directxmathvector.inl
api_name:
 - XMVectorCatmullRomV
---

# XMVectorCatmullRomV function


## -description

Performs a Catmull-Rom interpolation, using the specified position vectors.

## -parameters

### -param Position0 [in]

First position.

### -param Position1 [in]

Second position.

### -param Position2 [in]

Third position.

### -param Position3 [in]

Fourth position.

### -param T [in]

Interpolating control factor for the corresponding components of the position.

## -returns

Returns the results of the Catmull-Rom interpolation.

## -remarks

This function is identical to <a href="/windows/desktop/api/directxmath/nf-directxmath-xmvectorcatmullrom">XMVectorCatmullRom</a> except that independent weighting factors may supplied in <i>T</i>. As an example, you might want to calculate two sets of Catmull-Rom interpolation, using the x and y-components of the position vectors for one set of 2D positions and the z and w-components of the position vectors for the other set of 2D positions. The x and y-components of <i>T</i> would determine the interpolation factors for the first Catmull-Rom interpolation. Similarly, the z and w-components of <i>T</i> would determine the interpolation factors for the second Catmull-Rom interpolation.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-vector-geometric">Geometric Vector Functions</a>



<a href="/windows/desktop/api/directxmath/nf-directxmath-xmvectorcatmullrom">XMVectorCatmullRom</a>
