---
UID: NF:directxmath.XMVector4ClampLength
title: XMVector4ClampLength function (directxmath.h)
description: Clamps the length of a 4D vector to a given range.helpviewer_keywords: ["Use DirectX..XMVector4ClampLength","XMVector4ClampLength","XMVector4ClampLength method [DirectX Math Support APIs]","dxmath.xmvector4clamplength"]
old-location: dxmath\xmvector4clamplength.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.geometric.XMVector4ClampLength(XMVECTOR,float,float)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMVector4ClampLength, XMVector4ClampLength, XMVector4ClampLength method [DirectX Math Support APIs], dxmath.xmvector4clamplength
f1_keywords:
- directxmath/XMVector4ClampLength
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
- XMVector4ClampLength
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# XMVector4ClampLength function


## -description


Clamps the length of a 4D vector to a given range.


## -parameters




### -param V [in]

4D vector.


### -param LengthMin [in]

Minimum clamp length.


### -param LengthMax [in]

Maximum clamp length.


## -returns



Returns a 4D vector whose length is clamped to the specified minimum and maximum.




## -remarks



<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/dxmath/ovw-xnamath-reference-functions-vector4-geometric">DirectXMath Library 4D Vector Geometric Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/directxmath/nf-directxmath-xmvector4clamplengthv">XMVector4ClampLengthV</a>
 

 

