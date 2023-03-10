---
UID: NF:directxmath.XMVector4Normalize
title: XMVector4Normalize function (directxmath.h)
description: Returns the normalized version of a 4D vector.
helpviewer_keywords: ["Use DirectX..XMVector4Normalize","XMVector4Normalize","XMVector4Normalize method [DirectX Math Support APIs]","dxmath.xmvector4normalize"]
old-location: dxmath\xmvector4normalize.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.geometric.XMVector4Normalize(XMVECTOR)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMVector4Normalize, XMVector4Normalize, XMVector4Normalize method [DirectX Math Support APIs], dxmath.xmvector4normalize
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
 - XMVector4Normalize
 - directxmath/XMVector4Normalize
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
 - XMVector4Normalize
---

# XMVector4Normalize function


## -description

Returns the normalized version of a 4D vector.

## -parameters

### -param V [in]

4D vector.

## -returns

Returns the normalized version of <i>V</i>.

## -remarks

For a vector of length 0, this function returns a zero vector. For a vector with infinite length, it returns a vector of QNaN.

Note that for most graphics applications, ensuring the vectors have well-defined lengths that don't cause problems 
    for normalization is common practice. However, if you need a robust normalization that works for all floating-point inputs, 
    you can use the following code instead:


```

inline XMVECTOR XMVector4NormalizeRobust( FXMVECTOR V )
{
    // Compute the maximum absolute value component.
    XMVECTOR vAbs = XMVectorAbs(V);
    XMVECTOR max0 = XMVectorSplatX(vAbs);
    XMVECTOR max1 = XMVectorSplatY(vAbs);
    XMVECTOR max2 = XMVectorSplatZ(vAbs);
    XMVECTOR max3 = XMVectorSplatW(vAbs);
    max0 = XMVectorMax(max0, max1);
    max2 = XMVectorMax(max2, max3);
    max0 = XMVectorMax(max0, max2);

    // Divide by the maximum absolute component.
    XMVECTOR normalized = XMVectorDivide(V, max0);

    // Set to zero when the original length is zero.
    XMVECTOR mask = XMVectorNotEqual(g_XMZero, max0);
    normalized = XMVectorAndInt(normalized, mask);

    // (sqrLength, sqrLength, sqrLength, sqrLength)
    XMVECTOR t0 = XMVector4Dot(normalized, normalized);

    // (length, length, length, length)
    XMVECTOR length = XMVectorSqrt(t0);

    // Divide by the length to normalize.
    normalized = XMVectorDivide(normalized, length);

    // Set to zero when the original length is zero or infinity.  In the
    // latter case, this is considered to be an unexpected condition.
    normalized = XMVectorAndInt(normalized, mask);
    return normalized;
}
    
```


<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-vector4-geometric">DirectXMath Library 4D Vector Geometric Functions</a>



<a href="/windows/desktop/api/directxmath/nf-directxmath-xmvector4normalizeest">XMVector4NormalizeEst</a>