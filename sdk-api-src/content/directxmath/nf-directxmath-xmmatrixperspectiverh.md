---
UID: NF:directxmath.XMMatrixPerspectiveRH
title: XMMatrixPerspectiveRH function (directxmath.h)
description: Builds a right-handed perspective projection matrix.
helpviewer_keywords: ["Use DirectX..XMMatrixPerspectiveRH","XMMatrixPerspectiveRH","XMMatrixPerspectiveRH method [DirectX Math Support APIs]","dxmath.xmmatrixperspectiverh"]
old-location: dxmath\xmmatrixperspectiverh.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.matrix.XMMatrixPerspectiveRH(float,float,float,float)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMMatrixPerspectiveRH, XMMatrixPerspectiveRH, XMMatrixPerspectiveRH method [DirectX Math Support APIs], dxmath.xmmatrixperspectiverh
req.header: directxmath.h
req.include-header:
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
 - XMMatrixPerspectiveRH
 - directxmath/XMMatrixPerspectiveRH
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DirectXMath.h
api_name:
 - XMMatrixPerspectiveRH
---

# XMMatrixPerspectiveRH function


## -description

Builds a right-handed perspective projection matrix.

## -parameters

### -param ViewWidth [in]

Width of the frustum at the near clipping plane.

### -param ViewHeight [in]

Height of the frustum at the near clipping plane.

### -param NearZ [in]

Distance to the near clipping plane. Must be greater than zero.

### -param FarZ [in]

Distance to the far clipping plane. Must be greater than  zero.

## -returns

Returns the perspective projection matrix.

## -remarks

For typical usage, <i>NearZ</i> is less than <i>FarZ</i>. However, if you flip these values so <i>FarZ</i> is less than <i>NearZ</i>, the result is an inverted z buffer (also known as a "reverse z buffer") which can provide increased floating-point precision.

<i>NearZ</i> and <i>FarZ</i> cannot be the same value and must be greater than 0.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-matrix">DirectXMath Library Matrix Functions</a>



<a href="/windows/win32/api/directxmath/nf-directxmath-xmmatrixperspectivelh">XMMatrixPerspectiveLH</a>
