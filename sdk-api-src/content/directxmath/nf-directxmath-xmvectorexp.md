---
UID: NF:directxmath.XMVectorExp
title: XMVectorExp function (directxmath.h)
description: Computes two raised to the power for each component.Note  This function is a compatibility alias for XMVectorExp2 for existing Windows 8 code. This function is deprecated for Windows 8.1. Don't use it and instead use XMVectorExp2 or XMVectorExpE.  .
helpviewer_keywords: ["Use DirectX..XMVectorExp","XMVectorExp","XMVectorExp method [DirectX Math Support APIs]","dxmath.xmvectorexp"]
old-location: dxmath\xmvectorexp.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.transcendental.XMVectorExp(XMVECTOR)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMVectorExp, XMVectorExp, XMVectorExp method [DirectX Math Support APIs], dxmath.xmvectorexp
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
 - XMVectorExp
 - directxmath/XMVectorExp
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
 - XMVectorExp
---

# XMVectorExp function


## -description

Computes two raised to the power for each component.<div class="alert"><b>Note</b>  This function is a compatibility alias for <a href="/windows/desktop/api/directxmath/nf-directxmath-xmvectorexp2">XMVectorExp2</a> for existing Windows 8 code. This function is deprecated for Windows 8.1. Don't use it and instead use <b>XMVectorExp2</b> or <a href="/windows/desktop/api/directxmath/nf-directxmath-xmvectorexpe">XMVectorExpE</a>.
</div>
<div> </div>

## -parameters

### -param V [in]

Vector used for the exponents of base two.

## -returns

Returns a vector whose components are two raised to the power of the corresponding component of <i>V</i>.

## -remarks

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-vector-transcendental">Transcendental Vector Functions</a>