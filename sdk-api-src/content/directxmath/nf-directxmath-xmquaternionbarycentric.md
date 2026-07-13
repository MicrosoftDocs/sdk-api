---
UID: NF:directxmath.XMQuaternionBaryCentric
title: XMQuaternionBaryCentric function (directxmath.h)
description: Returns a point in barycentric coordinates, using the specified quaternions. (XMQuaternionBaryCentric)
helpviewer_keywords: ["Use DirectX..XMQuaternionBaryCentric","XMQuaternionBaryCentric","XMQuaternionBaryCentric method [DirectX Math Support APIs]","dxmath.xmquaternionbarycentric"]
old-location: dxmath\xmquaternionbarycentric.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.quaternion.XMQuaternionBaryCentric(XMVECTOR,XMVECTOR,XMVECTOR,float,float)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMQuaternionBaryCentric, XMQuaternionBaryCentric, XMQuaternionBaryCentric method [DirectX Math Support APIs], dxmath.xmquaternionbarycentric
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - XMQuaternionBaryCentric
 - directxmath/XMQuaternionBaryCentric
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DirectXMath.h
api_name:
 - XMQuaternionBaryCentric
---

# XMQuaternionBaryCentric function


## -description

Returns a point in barycentric coordinates, using the specified quaternions.

## -parameters

### -param Q0 [in]

First quaternion in the triangle.

### -param Q1 [in]

Second quaternion in the triangle.

### -param Q2 [in]

Third quaternion in the triangle.

### -param f [in]

Weighting factor. See the remarks.

### -param g [in]

Weighting factor. See the remarks.

## -returns

Returns a quaternion in barycentric coordinates.

## -remarks

The following pseudocode demonstrates the operation of the function.


```

XMVECTOR Result;
XMVECTOR QA, QB;
float s = f + g;

if (s != 0.0f)
{
    QA = XMQuaternionSlerp(Q0, Q1, s);
    QB = XMQuaternionSlerp(Q0, Q2, s);
    Result = XMQuaternionSlerp(QA, QB, g / s);
}
else
{
    Result.x = Q0.x;
    Result.y = Q0.y;
    Result.z = Q0.z;
    Result.w = Q0.w;
}

return Result;
        
```


Note that Barycentric coordinates work for 'flat' surfaces but not for 'curved' ones. This function is therefore a bit of a work-around.
        An alternative method for blending 3 quaternions is given by the following code:


```

inline XMVECTOR XMQuaternionBlend(FXMVECTOR Q0, FXMVECTOR Q1, FXMVECTOR Q2, float w1, float w2)
{
    // Note if you choose one of the three weights to be zero, you get a blend of two
    //  quaternions.  This does not give you slerp of those quaternions.
    float w0 = 1.0f - w1 - w2;
    XMVECTOR Result = XMVector4Normalize(
        XMVectorScale(Q0, w0) +
        XMVectorScale(Q1, w1) +
        XMVectorScale(Q2, w2));
    return Result;
}
        
```


<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-quaternion">DirectXMath Library Quaternion Functions</a>



<a href="/windows/desktop/api/directxmath/nf-directxmath-xmquaternionbarycentricv">XMQuaternionBaryCentricV</a>
