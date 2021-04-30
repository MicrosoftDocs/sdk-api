---
UID: NS:directxmath.XMUINT3
title: XMUINT3 (directxmath.h)
description: A 3D vector where each component is an unsigned integer.
helpviewer_keywords: ["XMUINT3","XMUINT3 structure [DirectX Math Support APIs]","directxmath/XMUINT3","dxmath.xmuint3"]
old-location: dxmath\xmuint3.htm
tech.root: dxmath
ms.assetid: T:Microsoft.directx_sdk.reference.XMUINT3
ms.date: 12/05/2018
ms.keywords: XMUINT3, XMUINT3 structure [DirectX Math Support APIs], directxmath/XMUINT3, dxmath.xmuint3
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
 - XMUINT3
 - directxmath/XMUINT3
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
 - XMUINT3
---

# XMUINT3 structure


## -description

A 3D vector where each component is an unsigned integer.

For a list of additional functionality such as constructors and operators that are available using <code>XMUINT3</code> when you
  are programming in C++, see <a href="/windows/desktop/dxmath/ovw-xmuint3-extensions">XMUINT3 Extensions</a>.
<div class="alert"><b>Note</b>  See <a href="/windows/desktop/dxmath/pg-xnamath-internals">DirectXMath Library Type Equivalences</a> for information about
  equivalent <a href="/windows/desktop/direct3d9/d3ddecltype">D3DDECLTYPE</a>, <a href="/windows/desktop/direct3d9/d3dformat">D3DFORMAT</a>, and
  <a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT</a> objects.</div><div> </div>

## -struct-fields

### -field x

Unsigned integer value describing the x-coordinate of the vector.

### -field y

Unsigned integer value describing the y-coordinate of the vector.

### -field z

Unsigned integer value describing the z-coordinate of the vector.

### -field operator=

TBD

### -field XMUINT3

TBD

## -remarks

You can use <a href="/windows/desktop/api/directxmath/nf-directxmath-xmloaduint3">XMLoadUInt3</a> to load <code>XMUINT3</code> into instances 
   of <a href="/windows/desktop/dxmath/xmvector-data-type">XMVECTOR</a>.

You can use <a href="/windows/desktop/api/directxmath/nf-directxmath-xmstoreuint3">XMStoreUInt3</a> to store instances of <code>XMVECTOR</code> 
     into an instance of <code>XMUINT3</code>.

<b>Namespace:</b> Use DirectX

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-structures">DirectXMath Library Structures</a>



<a href="/windows/desktop/dxmath/ovw-xmuint3-extensions">XMUINT3 Extensions</a>