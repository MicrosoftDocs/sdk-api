---
UID: NF:directxmath.XMVectorModAngles
title: XMVectorModAngles function (directxmath.h)
description: Computes the per-component angle modulo 2PI.
helpviewer_keywords: ["Use DirectX..XMVectorModAngles","XMVectorModAngles","XMVectorModAngles method [DirectX Math Support APIs]","dxmath.xmvectormodangles"]
old-location: dxmath\xmvectormodangles.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.geometric.XMVectorModAngles(XMVECTOR)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMVectorModAngles, XMVectorModAngles, XMVectorModAngles method [DirectX Math Support APIs], dxmath.xmvectormodangles
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
 - XMVectorModAngles
 - directxmath/XMVectorModAngles
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
 - XMVectorModAngles
---

# XMVectorModAngles function


## -description

Computes the per-component angle modulo 2PI.

## -parameters

### -param Angles [in]

Vector of angle components.

## -returns

Returns a vector whose components are the corresponding components of <i>Angles</i> modulo 2PI.

## -remarks

The following pseudocode demonstrates the operation of the function:


```
XMVECTOR result;

result.x = Angles.x - XM_2PI * round( Angles.x / XM_2PI );
result.y = Angles.y - XM_2PI * round( Angles.y / XM_2PI );
result.z = Angles.z - XM_2PI * round( Angles.z / XM_2PI );
result.w = Angles.w - XM_2PI * round( Angles.w / XM_2PI );

return result;
```


<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-vector-arithmetic">Vector Arithmetic Functions</a>