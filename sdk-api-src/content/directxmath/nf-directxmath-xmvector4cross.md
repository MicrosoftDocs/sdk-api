---
UID: NF:directxmath.XMVector4Cross
title: XMVector4Cross function (directxmath.h)
description: Computes the 4D cross product.
helpviewer_keywords: ["Use DirectX..XMVector4Cross","XMVector4Cross","XMVector4Cross method [DirectX Math Support APIs]","dxmath.xmvector4cross"]
old-location: dxmath\xmvector4cross.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.geometric.XMVector4Cross(XMVECTOR,XMVECTOR,XMVECTOR)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMVector4Cross, XMVector4Cross, XMVector4Cross method [DirectX Math Support APIs], dxmath.xmvector4cross
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
 - XMVector4Cross
 - directxmath/XMVector4Cross
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
 - XMVector4Cross
---

# XMVector4Cross function


## -description

Computes the 4D cross product.

## -parameters

### -param V1 [in]

4D vector.

### -param V2 [in]

4D vector.

### -param V3 [in]

4D vector.

## -returns

Returns the 4D cross product of <i>V1</i>, <i>V2</i>, and <i>V3</i>.

## -remarks

A 4D cross-product is not well-defined. This function computes a geometric analog to the 3D cross product. 
        <a href="/windows/desktop/api/directxmath/nf-directxmath-xmvector4orthogonal">XMVector4Orthogonal</a> is another generalized 'cross-product' for 4D vectors.

The following pseudocode demonstrates the operation of the function:


```

XMVECTOR Result;

Result.x = V1.y * (V2.z * V3.w - V3.z * V2.w)
           -  V1.z * (V2.y * V3.w - V3.y * V2.w )
           +  V1.w * (V2.y * V3.z - V3.y * V2.z);

Result.y = V1.x * (V3.z * V2.w - V2.z * V3.w)
           - V1.z * (V3.x * V2.w - V2.x * V3.w)
           + V1.w * (V3.x * V2.z - V2.x * V3.z);
                                    
Result.z = V1.x * (V2.y * V3.w - V3.y * V2.w)
           - V1.y * (V2.x * V3.w - V3.x * V2.w)
           + V1.w * (V2.x * V3.y - V3.x * V2.y);

Result.w = V1.x * (V3.y * V2.z - V2.y * V3.z)
           - V1.y * (V3.x * V2.z - V2.x * V3.z)
           + V1.z * (V3.x * V2.y - V2.x * V3.y);

return Result;
        
```


<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-vector4-geometric">DirectXMath Library 4D Vector Geometric Functions</a>