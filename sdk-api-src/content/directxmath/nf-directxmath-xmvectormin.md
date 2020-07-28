---
UID: NF:directxmath.XMVectorMin
title: XMVectorMin function (directxmath.h)
description: Makes a per-component comparison between two vectors, and returns a vector containing the smallest components.
helpviewer_keywords: ["Use DirectX..XMVectorMin","XMVectorMin","XMVectorMin method [DirectX Math Support APIs]","dxmath.xmvectormin"]
old-location: dxmath\xmvectormin.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.arithmetic.XMVectorMin(XMVECTOR,XMVECTOR)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMVectorMin, XMVectorMin, XMVectorMin method [DirectX Math Support APIs], dxmath.xmvectormin
f1_keywords:
- directxmath/XMVectorMin
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- directxmathvector.inl
api_name:
- XMVectorMin
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# XMVectorMin function


## -description


Makes a per-component comparison between two vectors, and returns a vector containing the smallest components.


## -parameters




### -param V1 [in]

First vector to compare.


### -param V2 [in]

Second vector to compare.


## -returns



Returns a vector containing the smallest components between the two vectors.




## -remarks



The following pseudocode demonstrates the operation of the function:


```
XMVECTOR Result;

Result.x = (V1.x < V2.x) ? V1.x : V2.x;
Result.y = (V1.y < V2.y) ? V1.y : V2.y;
Result.z = (V1.z < V2.z) ? V1.z : V2.z;
Result.w = (V1.w < V2.w) ? V1.w : V2.w;

return Result;
```


<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/dxmath/ovw-xnamath-reference-functions-vector-arithmetic">Vector Arithmetic Functions</a>
 

 

