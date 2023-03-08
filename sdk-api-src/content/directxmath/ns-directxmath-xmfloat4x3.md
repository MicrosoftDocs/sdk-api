---
UID: NS:directxmath.XMFLOAT4X3
title: XMFLOAT4X3 (directxmath.h)
description: A 4*3 floating point matrix.
helpviewer_keywords: ["XMFLOAT4X3","XMFLOAT4X3 structure [DirectX Math Support APIs]","directxmath/XMFLOAT4X3","dxmath.xmfloat4x3"]
old-location: dxmath\xmfloat4x3.htm
tech.root: dxmath
ms.assetid: T:Microsoft.directx_sdk.reference.XMFLOAT4X3
ms.date: 12/05/2018
ms.keywords: XMFLOAT4X3, XMFLOAT4X3 structure [DirectX Math Support APIs], directxmath/XMFLOAT4X3, dxmath.xmfloat4x3
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
 - XMFLOAT4X3
 - directxmath/XMFLOAT4X3
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
 - XMFLOAT4X3
---

# XMFLOAT4X3 structure


## -description

A 4*3 floating point matrix.



For a list of additional functionality such as constructors and operators that are available using <code>XMFLOAT4X3</code> when you
  are programming in C++, see <a href="/windows/win32/dxmath/ovw-xmfloat4x3-extensions">XMFLOAT4X3 Extensions</a>.
<div class="alert"><b>Note</b>  See <a href="/windows/desktop/dxmath/pg-xnamath-internals">DirectXMath Library Type Equivalences</a> for information about
  equivalent <a href="/windows/desktop/direct3d9/d3ddecltype">D3DDECLTYPE</a>, <a href="/windows/desktop/direct3d9/d3dformat">D3DFORMAT</a>, and
  <a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT</a> objects.</div><div> </div>

## -struct-fields

### -field _11

An element of the matrix.

### -field _12

An element of the matrix.

### -field _13

An element of the matrix.

### -field _21

An element of the matrix.

### -field _22

An element of the matrix.

### -field _23

An element of the matrix.

### -field _31

An element of the matrix.

### -field _32

An element of the matrix.

### -field _33

An element of the matrix.

### -field _41

An element of the matrix.

### -field _42

An element of the matrix.

### -field _43

An element of the matrix.

### -field m

A 4*3 array representing the matrix.

### -field f

### -field operator=

TBD

### -field XMFLOAT4X3

TBD

### -field operator()

TBD

## -remarks

Scalar members of <code>XMFLOAT4X3</code> are of the form <b>_</b><i>RowCol</i>, and provide one based indexing,
   where <i>Row</i> specifies the one's based matrix row (running from 1 to 4), and
   <i>Col</i> specifies the one's based matrix column (running from 1 to 3).

The two dimensional 4*3 array member of <code>XMFLOAT4X3</code>, <b>m</b>, provides zero based indexing of the structure's
   matrix. When accessing <code>XMFLOAT4X3</code><b>m[</b><i>Row</i><b>,</b><i>Col</i><b>]</b>, <i>Row</i> can run from 0 to 3 and <i>Col</i> can run from 0 to 2.

<code>XMFLOAT4X3</code> can be loaded into instances of <a href="/windows/desktop/dxmath/xmvector-data-type"> XMVECTOR</a> by using
   <a href="/windows/win32/api/directxmath/nf-directxmath-xmloadfloat4x3">XMLoadFloat4x3</a>.

Instances of <code>XMVECTOR</code> can be stored into an instance of <code>XMFLOAT4X3</code> with
   <a href="/windows/win32/api/directxmath/nf-directxmath-xmstorefloat4x3">XMStoreFloat4x3</a>.

<b>Namespace:</b> Use DirectX

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-structures">DirectXMath Library Structures</a>



<a href="/windows/win32/dxmath/ovw-xmfloat4x3-extensions">XMFLOAT4X3 Extensions</a>
