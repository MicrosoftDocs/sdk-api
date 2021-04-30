---
UID: NF:directxmath.XMLoadFloat2
title: XMLoadFloat2 function (directxmath.h)
description: Loads an XMFLOAT2 into an XMVECTOR.
helpviewer_keywords: ["Use DirectX..XMLoadFloat2","XMLoadFloat2","XMLoadFloat2 method [DirectX Math Support APIs]","dxmath.xmloadfloat2"]
old-location: dxmath\xmloadfloat2.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.loading.XMLoadFloat2(const XMFLOAT2)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMLoadFloat2, XMLoadFloat2, XMLoadFloat2 method [DirectX Math Support APIs], dxmath.xmloadfloat2
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
 - XMLoadFloat2
 - directxmath/XMLoadFloat2
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
 - XMLoadFloat2
---

# XMLoadFloat2 function


## -description

Loads an <a href="/windows/desktop/api/directxmath/ns-directxmath-xmfloat2">XMFLOAT2</a> into an <a href="/windows/desktop/dxmath/xmvector-data-type">XMVECTOR</a>.

## -parameters

### -param pSource [in]

Address of the <a href="/windows/desktop/api/directxmath/ns-directxmath-xmfloat2">XMFLOAT2</a> structure to load.

## -returns

Returns an <a href="/windows/desktop/dxmath/xmvector-data-type">XMVECTOR</a> loaded with the data from the <i>pSource</i> parameter.

## -remarks

The <b>x</b> and <b>y</b> members of the <a href="/windows/desktop/api/directxmath/ns-directxmath-xmfloat2">XMFLOAT2</a> are loaded into the
   corresponding members of the <a href="/windows/desktop/dxmath/xmvector-data-type">XMVECTOR</a>. The <b>z</b> and <b>w</b> members of the
   returned <b>XMVECTOR</b> will be initialized to 0.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-load">DirectXMath Library Vector Load Functions</a>