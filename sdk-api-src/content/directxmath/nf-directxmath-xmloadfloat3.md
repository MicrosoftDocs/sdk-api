---
UID: NF:directxmath.XMLoadFloat3
title: XMLoadFloat3 function (directxmath.h)
description: Loads an XMFLOAT3 into an XMVECTOR.
helpviewer_keywords: ["Use DirectX..XMLoadFloat3","XMLoadFloat3","XMLoadFloat3 method [DirectX Math Support APIs]","dxmath.xmloadfloat3"]
old-location: dxmath\xmloadfloat3.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.loading.XMLoadFloat3(const XMFLOAT3)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMLoadFloat3, XMLoadFloat3, XMLoadFloat3 method [DirectX Math Support APIs], dxmath.xmloadfloat3
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
 - XMLoadFloat3
 - directxmath/XMLoadFloat3
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
 - XMLoadFloat3
---

# XMLoadFloat3 function


## -description

Loads an <a href="/windows/desktop/api/directxmath/ns-directxmath-xmfloat3">XMFLOAT3</a> into an <a href="/windows/desktop/dxmath/xmvector-data-type">XMVECTOR</a>.

## -parameters

### -param pSource [in]

Address of the <a href="/windows/desktop/api/directxmath/ns-directxmath-xmfloat3">XMFLOAT3</a> structure to load.

## -returns

Returns an <a href="/windows/desktop/dxmath/xmvector-data-type">XMVECTOR</a> loaded with the data from the <i>pSource</i> parameter.

## -remarks

The <b>x</b>, <b>y</b> and <b>z</b> members of the <a href="/windows/desktop/api/directxmath/ns-directxmath-xmfloat3">XMFLOAT3</a> are loaded into
   the corresponding members of the <a href="/windows/desktop/dxmath/xmvector-data-type">XMVECTOR</a>. The <b>w</b> member of the returned
   <b>XMVECTOR</b> is initialized to 0.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-load">DirectXMath Library Vector Load Functions</a>