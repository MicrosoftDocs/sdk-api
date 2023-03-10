---
UID: NF:directxmath.XMVectorBaryCentricV
title: XMVectorBaryCentricV function (directxmath.h)
description: Returns a point in Barycentric coordinates, using the specified position vectors. (XMVectorBaryCentricV)
helpviewer_keywords: ["Use DirectX..XMVectorBaryCentricV","XMVectorBaryCentricV","XMVectorBaryCentricV method [DirectX Math Support APIs]","dxmath.xmvectorbarycentricv"]
old-location: dxmath\xmvectorbarycentricv.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.geometric.XMVectorBaryCentricV(XMVECTOR,XMVECTOR,XMVECTOR,XMVECTOR,XMVECTOR)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMVectorBaryCentricV, XMVectorBaryCentricV, XMVectorBaryCentricV method [DirectX Math Support APIs], dxmath.xmvectorbarycentricv
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
 - XMVectorBaryCentricV
 - directxmath/XMVectorBaryCentricV
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
 - XMVectorBaryCentricV
---

# XMVectorBaryCentricV function


## -description

Returns a point in Barycentric coordinates, using the specified position vectors.

## -parameters

### -param Position0 [in]

First position.

### -param Position1 [in]

Second position.

### -param Position2 [in]

Third position.

### -param F [in]

Weighting factors for the corresponding components of the position.

### -param G [in]

Weighting factors for the corresponding components of the position.

## -returns

Returns the Barycentric coordinates.

## -remarks

This function is identical to <a href="/windows/win32/api/directxmath/nf-directxmath-xmvectorbarycentric">XMVectorBaryCentric</a> except that independent weighting factors may supplied in <i>F</i> and <i>G</i>. As an example, you might want to calculate two sets of 2D Barycentric coordinates, using the x and y-components of the position vectors for one set of 2D positions and the z and w-components of the position vectors for the other set of 2D positions. The x and y-components of <i>F</i> and <i>G</i> would determine the weighting factors for the first set of Barycentric coordinates. Similarly, the z and w-components of <i>F</i> and <i>G</i> would determine the weighting factors for the second set of Barycentric coordinates.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-vector-geometric">Geometric Vector Functions</a>



<a href="/windows/win32/api/directxmath/nf-directxmath-xmvectorbarycentric">XMVectorBaryCentric</a>
