---
UID: NF:directxmath.XMVectorMergeXY
title: XMVectorMergeXY function (directxmath.h)
description: Creates a new vector by combining the x and y-components of two vectors.
helpviewer_keywords: ["Use DirectX..XMVectorMergeXY","XMVectorMergeXY","XMVectorMergeXY method [DirectX Math Support APIs]","dxmath.xmvectormergexy"]
old-location: dxmath\xmvectormergexy.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.component-wise.XMVectorMergeXY(XMVECTOR,XMVECTOR)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMVectorMergeXY, XMVectorMergeXY, XMVectorMergeXY method [DirectX Math Support APIs], dxmath.xmvectormergexy
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
 - XMVectorMergeXY
 - directxmath/XMVectorMergeXY
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
 - XMVectorMergeXY
---

# XMVectorMergeXY function


## -description

Creates a new vector by combining the x and y-components of two vectors.

## -parameters

### -param V1 [in]

First vector.

### -param V2 [in]

Second vector.

## -returns

Returns the merged vector.

## -remarks

The following pseudocode demonstrates the operation of the function:


```
XMVECTOR Result;

Result.x = V1.x;
Result.y = V2.x;
Result.z = V1.y;
Result.w = V2.y;

return Result;
```


<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-vector-component-wise">Component-Wise Vector Functions</a>



<a href="/windows/desktop/api/directxmath/nf-directxmath-xmvectormergezw">XMVectorMergeZW</a>