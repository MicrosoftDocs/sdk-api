---
UID: NF:directxmath.XMVector3Cross
title: XMVector3Cross function (directxmath.h)
description: Computes the cross product between two 3D vectors.
helpviewer_keywords: ["Use DirectX..XMVector3Cross","XMVector3Cross","XMVector3Cross method [DirectX Math Support APIs]","dxmath.xmvector3cross"]
old-location: dxmath\xmvector3cross.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.geometric.XMVector3Cross(XMVECTOR,XMVECTOR)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMVector3Cross, XMVector3Cross, XMVector3Cross method [DirectX Math Support APIs], dxmath.xmvector3cross
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
 - XMVector3Cross
 - directxmath/XMVector3Cross
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
 - XMVector3Cross
---

# XMVector3Cross function


## -description

Computes the cross product between two 3D vectors.

## -parameters

### -param V1 [in]

3D vector.

### -param V2 [in]

3D vector.

## -returns

Returns the cross product of <i>V1</i> and <i>V2</i>.

## -remarks

The following pseudocode demonstrates the operation of the function:


```

XMVECTOR Result;
Result.x = (V1.y * V2.z) - (V1.z * V2.y);
Result.y = (V1.z * V2.x) - (V1.x * V2.z);
Result.z = (V1.x * V2.y) - (V1.y * V2.x);
Result.w = 0;
return Result;
    
```


<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-vector3-geometric">DirectXMath Library 3D Vector Geometric Functions</a>