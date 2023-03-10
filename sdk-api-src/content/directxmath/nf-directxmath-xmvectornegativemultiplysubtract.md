---
UID: NF:directxmath.XMVectorNegativeMultiplySubtract
title: XMVectorNegativeMultiplySubtract function (directxmath.h)
description: Computes the difference of a third vector and the product of the first two vectors.
helpviewer_keywords: ["Use DirectX..XMVectorNegativeMultiplySubtract","XMVectorNegativeMultiplySubtract","XMVectorNegativeMultiplySubtract method [DirectX Math Support APIs]","dxmath.xmvectornegativemultiplysubtract"]
old-location: dxmath\xmvectornegativemultiplysubtract.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.arithmetic.XMVectorNegativeMultiplySubtract(XMVECTOR,XMVECTOR,XMVECTOR)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMVectorNegativeMultiplySubtract, XMVectorNegativeMultiplySubtract, XMVectorNegativeMultiplySubtract method [DirectX Math Support APIs], dxmath.xmvectornegativemultiplysubtract
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
 - XMVectorNegativeMultiplySubtract
 - directxmath/XMVectorNegativeMultiplySubtract
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
 - XMVectorNegativeMultiplySubtract
---

# XMVectorNegativeMultiplySubtract function


## -description

Computes the difference of a third vector and the product of the first two vectors.

## -parameters

### -param V1 [in]

Vector multiplier.

### -param V2 [in]

Vector multiplicand.

### -param V3 [in]

Vector subtrahend.

## -returns

Returns the resulting vector. See the remarks.

## -remarks

The following pseudocode demonstrates the operation of the function:


```
XMVECTOR result;

result.x = V3.x - V1.x * V2.x;
result.y = V3.y - V1.y * V2.y;
result.z = V3.z - V1.z * V2.z;
result.w = V3.w - V1.w * V2.w;

return result;
```


<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-vector-arithmetic">Vector Arithmetic Functions</a>