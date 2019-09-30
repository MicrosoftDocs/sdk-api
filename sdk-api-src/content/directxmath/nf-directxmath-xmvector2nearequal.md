---
UID: NF:directxmath.XMVector2NearEqual
title: XMVector2NearEqual function (directxmath.h)
author: windows-sdk-content
description: Tests whether one 2D vector is near another 2D vector.
old-location: dxmath\xmvector2nearequal.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.comparison.XMVector2NearEqual(XMVECTOR,XMVECTOR,XMVECTOR)
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMVector2NearEqual, XMVector2NearEqual, XMVector2NearEqual method [DirectX Math Support APIs], dxmath.xmvector2nearequal
ms.topic: function
f1_keywords: 
 - "directxmath/XMVector2NearEqual"
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
 - XMVector2NearEqual
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# XMVector2NearEqual function


## -description


Tests whether one 2D vector is near another 2D vector.


## -parameters




### -param V1 [in]

2D vector.


### -param V2 [in]

2D vector.


### -param Epsilon [in]

Tolerance value used for judging equality.


## -returns



Returns true if the difference between components is less than <i>Epsilon</i>; returns false otherwise.




## -remarks



The following pseudocode demonstrates the operation of the function:


```
return ( ( abs( V1.x - V2.x ) <= Epsilon ) && 
         ( abs( V1.y - V2.y ) <= Epsilon ) );
```


<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/dxmath/ovw-xnamath-reference-functions-vector2-comparison">DirectXMath Library 2D Vector Comparison Functions</a>
 

 

