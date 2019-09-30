---
UID: NF:directxmath.XMVector4ClampLengthV
title: XMVector4ClampLengthV function (directxmath.h)
author: windows-sdk-content
description: Clamps the length of a 4D vector to a given range.
old-location: dxmath\xmvector4clamplengthv.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.geometric.XMVector4ClampLengthV(XMVECTOR,XMVECTOR,XMVECTOR)
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMVector4ClampLengthV, XMVector4ClampLengthV, XMVector4ClampLengthV method [DirectX Math Support APIs], dxmath.xmvector4clamplengthv
ms.topic: function
f1_keywords: 
 - "directxmath/XMVector4ClampLengthV"
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
 - XMVector4ClampLengthV
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# XMVector4ClampLengthV function


## -description


Clamps the length of a 4D vector to a given range.


## -parameters




### -param V [in]

4D vector to clamp.


### -param LengthMin [in]

4D vector, all of whose components are equal to the minimum clamp length. The components must be greater-than-or-equal to zero.


### -param LengthMax [in]

4D vector, all of whose components are equal to the maximum clamp length. The components must be greater-than-or-equal to zero.


## -returns



Returns a 4D vector whose length is clamped to the specified minimum and maximum.




## -remarks



This function is identical to <a href="https://docs.microsoft.com/en-us/windows/desktop/api/directxmath/nf-directxmath-xmvector4clamplength">XMVector4ClampLength</a> except that <i>LengthMin</i> and <i>LengthMax</i> are supplied using 4D vectors instead of <b>float</b> values.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/dxmath/ovw-xnamath-reference-functions-vector4-geometric">DirectXMath Library 4D Vector Geometric Functions</a>



<a href="https://docs.microsoft.com/en-us/windows/desktop/api/directxmath/nf-directxmath-xmvector4clamplength">XMVector4ClampLength</a>
 

 

