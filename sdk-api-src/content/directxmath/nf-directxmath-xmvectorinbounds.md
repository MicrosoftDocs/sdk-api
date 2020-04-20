---
UID: NF:directxmath.XMVectorInBounds
title: XMVectorInBounds function (directxmath.h)
description: Tests whether the components of a given vector are within set bounds.helpviewer_keywords: ["Use DirectX..XMVectorInBounds","XMVectorInBounds","XMVectorInBounds method [DirectX Math Support APIs]","dxmath.xmvectorinbounds"]
old-location: dxmath\xmvectorinbounds.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.geometric.XMVectorInBounds(XMVECTOR,XMVECTOR)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMVectorInBounds, XMVectorInBounds, XMVectorInBounds method [DirectX Math Support APIs], dxmath.xmvectorinbounds
f1_keywords:
- directxmath/XMVectorInBounds
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
- XMVectorInBounds
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# XMVectorInBounds function


## -description


Tests whether the components of a given vector are within set bounds.


## -parameters




### -param V [in]

Vector to test.


### -param Bounds [in]

Vector that determines the bounds.


## -returns



Returns a vector containing the results of each component test.




## -remarks



The following pseudocode demonstrates the operation of the function:


```
XMVECTOR Control;

Control.x = (V.x <= Bounds.x && V.x >= -Bounds.x) ? 0xFFFFFFFF : 0;
Control.y = (V.y <= Bounds.y && V.y >= -Bounds.y) ? 0xFFFFFFFF : 0;
Control.z = (V.z <= Bounds.z && V.z >= -Bounds.z) ? 0xFFFFFFFF : 0;
Control.w = (V.w <= Bounds.w && V.w >= -Bounds.w) ? 0xFFFFFFFF : 0;

return Control;
```


<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/dxmath/ovw-xnamath-reference-functions-vector-geometric">Geometric Vector Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/directxmath/nf-directxmath-xmvectorinboundsr">XMVectorInBoundsR</a>
 

 

