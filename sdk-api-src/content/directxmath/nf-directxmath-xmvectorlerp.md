---
UID: NF:directxmath.XMVectorLerp
title: XMVectorLerp function (directxmath.h)
description: Performs a linear interpolation between two vectors. (XMVectorLerp)
helpviewer_keywords: ["Use DirectX..XMVectorLerp","XMVectorLerp","XMVectorLerp method [DirectX Math Support APIs]","dxmath.xmvectorlerp"]
old-location: dxmath\xmvectorlerp.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.geometric.XMVectorLerp(XMVECTOR,XMVECTOR,float)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMVectorLerp, XMVectorLerp, XMVectorLerp method [DirectX Math Support APIs], dxmath.xmvectorlerp
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
 - XMVectorLerp
 - directxmath/XMVectorLerp
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
 - XMVectorLerp
---

# XMVectorLerp function


## -description

Performs a linear interpolation between two vectors.

## -parameters

### -param V0 [in]

First vector to interpolate from.

### -param V1 [in]

Second vector to interpolate from.

### -param t [in]

Interpolation control factor.

## -returns

Returns a vector containing the interpolation.

## -remarks

The following pseudocode demonstrates the operation of the function:


```
XMVECTOR Result;

Result.x = V0.x + t * (V1.x - V0.x);
Result.y = V0.y + t * (V1.y - V0.y);
Result.z = V0.z + t * (V1.z - V0.z);
Result.w = V0.w + t * (V1.w - V0.w);

return Result;
```


Note it is fairly simple to use this function for doing a cubic interpolation instead of a linear interpolation as
   follows:


```

XMVECTOR SmoothStep( XMVECTOR V0, XMVECTOR V1, float t )
{
    t = (t > 1.0f) ? 1.0f : ((t < 0.0f) ? 0.0f : t);  // Clamp value to 0 to 1
    t = t*t*(3.f - 2.f*t);
    return XMVectorLerp( V0, V1, t );
}

```


<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-vector-geometric">Geometric Vector Functions</a>



<a href="/windows/desktop/api/directxmath/nf-directxmath-xmvectorlerpv">XMVectorLerpV</a>
