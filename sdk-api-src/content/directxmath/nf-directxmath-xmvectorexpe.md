---
UID: NF:directxmath.XMVectorExpE
title: XMVectorExpE function (directxmath.h)
description: Computes e (~2.71828) raised to the power for each component.
helpviewer_keywords: ["Use DirectX..XMVectorExpE","XMVectorExpE","XMVectorExpE method [DirectX Math Support APIs]","dxmath.xmvectorexpe"]
old-location: dxmath\xmvectorexpe.htm
tech.root: dxmath
ms.assetid: C4A5E4E0-56CC-46E3-87C5-CA99EF512B11
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMVectorExpE, XMVectorExpE, XMVectorExpE method [DirectX Math Support APIs], dxmath.xmvectorexpe
f1_keywords:
- directxmath/XMVectorExpE
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
- XMVectorExpE
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# XMVectorExpE function


## -description


Computes e (~2.71828) raised to the power for each component.


## -parameters




### -param V [in]

Vector used for the exponents of base e.


## -returns



Returns a vector whose components are e raised to the power of the corresponding component of <i>V</i>.





## -remarks



<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8.1. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

<b>XMVectorExpE</b> is new for DirectXMath version 3.05. 

It's similar to the existing <a href="https://docs.microsoft.com/windows/desktop/api/directxmath/nf-directxmath-xmvectorexp">XMVectorExp</a> function for Windows 8, but computes base e instead of base 2.


<b>XMVectorExpE</b> is implemented like this:

<pre class="syntax" xml:space="preserve"><code>
XMVECTOR Result; 

Result.x = expf(V.x);
Result.y = expf(V.y);
Result.z = expf(V.z);
Result.w = expf(V.w);

return Result;
</code></pre>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/dxmath/ovw-xnamath-reference-functions-vector-transcendental">Transcendental Vector Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/directxmath/nf-directxmath-xmvectorexp2">XMVectorExp2</a>



<a href="https://docs.microsoft.com/windows/desktop/api/directxmath/nf-directxmath-xmvectorloge">XMVectorLogE</a>
 

 

