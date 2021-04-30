---
UID: NS:directxmath.XMFLOAT3
title: XMFLOAT3 (directxmath.h)
description: Describes a 3D vector consisting of three single-precision floating-point values.
helpviewer_keywords: ["XMFLOAT3","XMFLOAT3 structure [DirectX Math Support APIs]","directxmath/XMFLOAT3","dxmath.xmfloat3"]
old-location: dxmath\xmfloat3.htm
tech.root: dxmath
ms.assetid: T:Microsoft.directx_sdk.reference.XMFLOAT3
ms.date: 12/05/2018
ms.keywords: XMFLOAT3, XMFLOAT3 structure [DirectX Math Support APIs], directxmath/XMFLOAT3, dxmath.xmfloat3
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
req.namespace: 
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
 - XMFLOAT3
 - directxmath/XMFLOAT3
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - DirectXMath.h
api_name:
 - XMFLOAT3
---

# XMFLOAT3 structure


## -description

Describes a 3D vector consisting of three single-precision floating-point values.

For a list of additional functionality such as constructors and operators that are available using <code>XMFLOAT3</code> when you
  are programming in C++, see <a href="/windows/desktop/dxmath/ovw-xmfloat3-extensions">XMFLOAT3 Extensions</a>.
<div class="alert"><b>Note</b>  See <a href="/windows/desktop/dxmath/pg-xnamath-internals">DirectXMath Library Type Equivalences</a> for information
  about equivalent <a href="/windows/desktop/direct3d9/d3ddecltype">D3DDECLTYPE</a>, <a href="/windows/desktop/direct3d9/d3dformat">D3DFORMAT</a>, and
  <a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT</a> objects.</div><div> </div>

## -struct-fields

### -field x

<b>float</b> value describing the x-coordinate of the vector.

### -field y

<b>float</b> value describing the y-coordinate of the vector.

### -field z

<b>float</b> value describing the z-coordinate of the vector.

### -field operator=

TBD

### -field XMFLOAT3

TBD

## -remarks

<code>XMFLOAT3</code> can be loaded into instances of <a href="/windows/desktop/dxmath/xmvector-data-type"> XMVECTOR</a> by using
   <a href="/windows/desktop/api/directxmath/nf-directxmath-xmloadfloat3">XMLoadFloat3</a>.

Instances of <code>XMVECTOR</code> can be stored into an instance of <code>XMFLOAT3</code> with
   <a href="/windows/desktop/api/directxmath/nf-directxmath-xmstorefloat3">XMStoreFloat3</a>.

<b>Namespace:</b> Use DirectX

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-structures">DirectXMath Library Structures</a>



<a href="/windows/desktop/dxmath/ovw-xmfloat3-extensions">XMFLOAT3 Extensions</a>