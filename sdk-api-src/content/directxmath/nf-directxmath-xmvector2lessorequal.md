---
UID: NF:directxmath.XMVector2LessOrEqual
title: XMVector2LessOrEqual function (directxmath.h)
description: Tests whether one 2D vector is less-than-or-equal-to another 2D vector.helpviewer_keywords: ["Use DirectX..XMVector2LessOrEqual","XMVector2LessOrEqual","XMVector2LessOrEqual method [DirectX Math Support APIs]","dxmath.xmvector2lessorequal"]
old-location: dxmath\xmvector2lessorequal.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.comparison.XMVector2LessOrEqual(XMVECTOR,XMVECTOR)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMVector2LessOrEqual, XMVector2LessOrEqual, XMVector2LessOrEqual method [DirectX Math Support APIs], dxmath.xmvector2lessorequal
f1_keywords:
- directxmath/XMVector2LessOrEqual
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
- XMVector2LessOrEqual
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# XMVector2LessOrEqual function


## -description


Tests whether one 2D vector is less-than-or-equal-to another 2D vector.


## -parameters




### -param V1 [in]

2D vector.


### -param V2 [in]

2D vector.


## -returns



Returns true if <i>V1</i> is less-than-or-equal to <i>V2</i>, and false otherwise. See the remarks section.




## -remarks



The following pseudocode demonstrates the operation of the function:


```
return ( V1.x <= V2.x && V1.y <= V2.y );
```


<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/dxmath/ovw-xnamath-reference-functions-vector2-comparison">DirectXMath Library 2D Vector Comparison Functions</a>
 

 

