---
UID: NF:directxmath.XMVectorCatmullRom
title: XMVectorCatmullRom function (directxmath.h)
description: Performs a Catmull-Rom interpolation, using the specified position vectors. (XMVectorCatmullRom)
helpviewer_keywords: ["Use DirectX..XMVectorCatmullRom","XMVectorCatmullRom","XMVectorCatmullRom method [DirectX Math Support APIs]","dxmath.xmvectorcatmullrom"]
old-location: dxmath\xmvectorcatmullrom.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.geometric.XMVectorCatmullRom(XMVECTOR,XMVECTOR,XMVECTOR,XMVECTOR,float)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMVectorCatmullRom, XMVectorCatmullRom, XMVectorCatmullRom method [DirectX Math Support APIs], dxmath.xmvectorcatmullrom
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
 - XMVectorCatmullRom
 - directxmath/XMVectorCatmullRom
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
 - XMVectorCatmullRom
---

# XMVectorCatmullRom function


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

### -param t [in]

Interpolating control factor.

## -returns

Returns the results of the Catmull-Rom interpolation.

## -remarks

The following pseudocode demonstrates the operation of the function:


```
XMVECTOR Result;

float t2 = t * t;
float t3 = t2* t;

float P0 = -t3 + 2.0f * t2 - t;
float P1 = 3.0f * t3 - 5.0f * t2 + 2.0f;
float P2 = -3.0f * t3 + 4.0f * t2 + t;
float P3 = t3 - t2;

Result.x = (P0 * Position0.x + P1 * Position1.x + P2 * Position2.x + P3 * Position3.x) * 0.5f;
Result.y = (P0 * Position0.y + P1 * Position1.y + P2 * Position2.y + P3 * Position3.y) * 0.5f;
Result.z = (P0 * Position0.z + P1 * Position1.z + P2 * Position2.z + P3 * Position3.z) * 0.5f;
Result.w = (P0 * Position0.w + P1 * Position1.w + P2 * Position2.w + P3 * Position3.w) * 0.5f;

return Result;
```


<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-vector-geometric">Geometric Vector Functions</a>



<a href="/windows/desktop/api/directxmath/nf-directxmath-xmvectorcatmullromv">XMVectorCatmullRomV</a>
