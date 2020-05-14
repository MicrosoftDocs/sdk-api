---
UID: NF:directxmath.XMVectorCeiling
title: XMVectorCeiling function (directxmath.h)
description: Computes the ceiling of each component of an XMVECTOR.helpviewer_keywords: ["Use DirectX..XMVectorCeiling","XMVectorCeiling","XMVectorCeiling method [DirectX Math Support APIs]","dxmath.xmvectorceiling"]
old-location: dxmath\xmvectorceiling.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.arithmetic.XMVectorCeiling(XMVECTOR)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMVectorCeiling, XMVectorCeiling, XMVectorCeiling method [DirectX Math Support APIs], dxmath.xmvectorceiling
f1_keywords:
- directxmath/XMVectorCeiling
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
- XMVectorCeiling
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# XMVectorCeiling function


## -description


Computes the ceiling of each component of an <a href="https://docs.microsoft.com/windows/desktop/dxmath/xmvector-data-type">XMVECTOR</a>.


## -parameters




### -param V [in]

Vector for which to compute the ceiling.


## -returns



Returns a vector whose components are the ceiling of the corresponding components of <i>V</i>.




## -remarks



<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

<b>XMVectorCeiling</b> is implemented like this:

<pre class="syntax" xml:space="preserve"><code>
XMVECTOR Result; 
Result.x = ceilf(V.x); 
Result.y = ceilf(V.y); 
Result.z = ceilf(V.z); 
Result.w = ceilf(V.w); 
return Result; 
</code></pre>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/dxmath/ovw-xnamath-reference-functions-vector-arithmetic">Vector Arithmetic Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/directxmath/nf-directxmath-xmvectorfloor">XMVectorFloor</a>
 

 

