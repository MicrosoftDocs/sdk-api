---
UID: NS:directxmath.XMFLOAT2A
title: XMFLOAT2A
description: Describes an XMFLOAT2 structure aligned on a 16-byte boundary.
tech.root: dxmath
helpviewer_keywords: ["XMFLOAT2A"]
ms.assetid: 9717e83e-b8d8-4855-9e53-e54f946fdd97
ms.date: 05/20/2019
ms.keywords: XMFLOAT2A
f1_keywords:
- directxmath/XMFLOAT2A
dev_langs:
- c++
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
topic_type:
- apiref
api_type:
- HeaderDef
api_location:
- directxmath.h
api_name:
- XMFLOAT2A
---

# XMFLOAT2A Structure

## -description

Describes an <a href="https://docs.microsoft.com/windows/desktop/api/directxmath/ns-directxmath-xmfloat2">XMFLOAT2</a> structure aligned on a 16-byte boundary.

<div class="alert"><b>Note</b>  See <a href="https://docs.microsoft.com/windows/desktop/dxmath/pg-xnamath-internals">DirectXMath Library Type Equivalences</a> for information about equivalent <a href="https://msdn.microsoft.com/993fc7e4-4752-4bce-82d0-0a034fdc69c0">D3DDECLTYPE</a>, <a href="https://msdn.microsoft.com/a222e3bb-310c-4019-93ee-6a2da2a46ded">D3DFORMAT</a>, and <a href="https://msdn.microsoft.com/dce61bc4-4ed5-4e64-84e8-6db88025e5c2">DXGI_FORMAT</a> objects.</div>

## -struct-fields

### -field XMFLOAT2

An **XMFLOAT2** object.

## -remarks

<code>XMFLOAT2A</code> can be loaded into instances of <a href="https://docs.microsoft.com/windows/desktop/dxmath/xmvector-data-type">XMVECTOR</a> by using <a href="https://docs.microsoft.com/windows/desktop/api/directxmath/nf-directxmath-xmloadfloat2a">XMLoadFloat2A</a>.

Instances of <code>XMVECTOR</code> can be stored into an instance of <code>XMFLOAT2A</code> with **XMStoreFloat2A**.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3> Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="https://docs.microsoft.com/windows/desktop/dxmath/ovw-xnamath-reference-structures">DirectXMath Library Structures</a>

<a href="https://docs.microsoft.com/windows/desktop/api/directxmath/ns-directxmath-xmfloat2">XMFLOAT2</a>
