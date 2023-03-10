---
UID: NF:directxmath.XMVectorLog
title: XMVectorLog function (directxmath.h)
description: Computes the base two logarithm of each component of a vector.Note  This function is a compatibility alias for XMVectorLog2 for existing Windows 8 code.
helpviewer_keywords: ["Use DirectX..XMVectorLog","XMVectorLog","XMVectorLog method [DirectX Math Support APIs]","dxmath.xmvectorlog"]
old-location: dxmath\xmvectorlog.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.transcendental.XMVectorLog(XMVECTOR)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMVectorLog, XMVectorLog, XMVectorLog method [DirectX Math Support APIs], dxmath.xmvectorlog
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
 - XMVectorLog
 - directxmath/XMVectorLog
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
 - XMVectorLog
---

# XMVectorLog function


## -description

Computes the base two logarithm of each component of a vector.<div class="alert"><b>Note</b>  This function is a compatibility alias for <a href="/windows/desktop/api/directxmath/nf-directxmath-xmvectorlog2">XMVectorLog2</a> for existing Windows 8 code. This function is deprecated for Windows 8.1. Don't use it and instead use <b>XMVectorLog2</b> or <a href="/windows/desktop/api/directxmath/nf-directxmath-xmvectorloge">XMVectorLogE</a>.
</div>
<div> </div>

## -parameters

### -param V [in]

Vector for which to compute the base two logarithm.

## -returns

Returns a vector whose components are base two logarithm of the corresponding components of <i>V</i>.

## -remarks

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-vector-transcendental">Transcendental Vector Functions</a>