---
UID: NS:directxmath.XMFLOAT3A
title: XMFLOAT3A
description: Describes an XMFLOAT3 structure aligned on a 16-byte boundary.
tech.root: dxmath
helpviewer_keywords: ["XMFLOAT3A"]
ms.assetid: bad51162-3eaa-44e1-9032-6db3e75f0e99
ms.date: 05/20/2019
ms.keywords: XMFLOAT3A
targetos: Windows
req.construct-type: structure
req.ddi-compliance:
req.dll:
req.header: directxmath.h
req.include-header:
req.kmdf-ver:
req.lib:
req.max-support:
req.redist:
req.target-min-winverclnt:
req.target-min-winversvr:
req.target-type:
req.typenames:
req.umdf-ver:
req.unicode-ansi:
f1_keywords:
 - XMFLOAT3A
 - directxmath/XMFLOAT3A
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - directxmath.h
api_name:
 - XMFLOAT3A
---

# XMFLOAT3A structure


## -description

Describes an <a href="/windows/win32/api/directxmath/ns-directxmath-xmfloat3">XMFLOAT3</a> structure aligned on a 16-byte boundary.

<div class="alert"><b>Note</b>  See <a href="/windows/desktop/dxmath/pg-xnamath-internals">DirectXMath Library Type Equivalences</a> for information
  about equivalent <a href="/windows/desktop/direct3d9/d3ddecltype">D3DDECLTYPE</a>, <a href="/windows/desktop/direct3d9/d3dformat">D3DFORMAT</a>, and
  <a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT</a> objects.</div>

## -struct-fields

### -field XMFLOAT3

An **XMFLOAT3** object.

## -remarks

<code>XMFLOAT3A</code> can be loaded into instances of <a href="/windows/desktop/dxmath/xmvector-data-type">XMVECTOR</a> by using <a href="/windows/win32/api/directxmath/nf-directxmath-xmloadfloat3a">XMLoadFloat3A</a>.

Instances of <code>XMVECTOR</code> can be stored into an instance of <code>XMFLOAT3A</code> with <a href="/windows/win32/api/directxmath/nf-directxmath-xmstorefloat3a">XMStoreFloat3A</a>.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-structures">DirectXMath Library Structures</a>

<a href="/windows/win32/api/directxmath/ns-directxmath-xmfloat3">XMFLOAT3</a>
