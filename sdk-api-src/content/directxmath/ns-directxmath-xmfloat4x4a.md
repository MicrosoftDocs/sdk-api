---
UID: NS:directxmath.XMFLOAT4X4A
title: XMFLOAT4X4A
description: Describes an XMFLOAT4X4 structure aligned on a 16-byte boundary.
tech.root: dxmath
helpviewer_keywords: ["XMFLOAT4X4A"]
ms.assetid: 30563f47-6990-4d94-a587-5c64a389762f
ms.date: 05/20/2019
ms.keywords: XMFLOAT4X4A
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
 - XMFLOAT4X4A
 - directxmath/XMFLOAT4X4A
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - directxmath.h
api_name:
 - XMFLOAT4X4A
---

# XMFLOAT4X4A Structure


## -description

Describes an <a href="/windows/desktop/api/directxmath/ns-directxmath-xmfloat4x4">XMFLOAT4X4</a> structure aligned on a 16-byte boundary.

<div class="alert"><b>Note</b>  See <a href="/windows/desktop/dxmath/pg-xnamath-internals">DirectXMath Library Type Equivalences</a> for information about equivalent <a href="/windows/desktop/direct3d9/d3ddecltype">D3DDECLTYPE</a>, <a href="/windows/desktop/direct3d9/d3dformat">D3DFORMAT</a>, and
<a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT</a> objects.</div>

## -struct-fields

### -field XMFLOAT4X4

An **XMFLOAT4X4** object.

## -remarks

<code>XMFLOAT4X4A</code> can be loaded into instances of <a href="/windows/desktop/dxmath/xmvector-data-type">XMVECTOR</a> by using **XMLoadFloat4x4A**.

Instances of <code>XMVECTOR</code> can be stored into an instance of <code>XMFLOAT4X4A</code> with **XMStoreFloat4x4A**.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3> Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-structures">DirectXMath Library Structures</a>

<a href="/windows/desktop/api/directxmath/ns-directxmath-xmfloat4x4">XMFLOAT4X4</a>
