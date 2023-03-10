---
UID: NS:directxpackedvector.XMUBYTE2
title: XMUBYTE2 (directxpackedvector.h)
description: Describes a 2D vector where each component is a unsigned integer, 8-bits (1 byte) in length.
helpviewer_keywords: ["XMUBYTE2","XMUBYTE2 structure [DirectX Math Support APIs]","_XMUBYTE2","_XMUBYTE2 structure [DirectX Math Support APIs]","directxpackedvector/XMUBYTE2","dxmath.xmubyte2"]
old-location: dxmath\xmubyte2.htm
tech.root: dxmath
ms.assetid: T:Microsoft.directx_sdk.reference.XMUBYTE2
ms.date: 12/05/2018
ms.keywords: XMUBYTE2, XMUBYTE2 structure [DirectX Math Support APIs], _XMUBYTE2, _XMUBYTE2 structure [DirectX Math Support APIs], directxpackedvector/XMUBYTE2, dxmath.xmubyte2
req.header: directxpackedvector.h
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
 - XMUBYTE2
 - directxpackedvector/XMUBYTE2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - DirectXPackedVector.h
api_name:
 - _XMUBYTE2
---

# XMUBYTE2 structure


## -description

Describes a 2D vector where each component is a unsigned integer, 8-bits (1 byte) in length.

A 2D vector where each component is a unsigned integer, 8-bits (1 byte) in length.



For a list of additional functionality such as constructors and operators that are available using <code>XMUBYTE2</code> when you
  are programming in C++, see <a href="/windows/desktop/dxmath/ovw-xmubyte2-extensions">XMUBYTE2 Extensions</a>.
<div class="alert"><b>Note</b>  See <a href="/windows/desktop/dxmath/pg-xnamath-internals">DirectXMath Library Type Equivalences</a> for information about
  equivalent <a href="/windows/desktop/direct3d9/d3ddecltype">D3DDECLTYPE</a>, <a href="/windows/desktop/direct3d9/d3dformat">D3DFORMAT</a>, and
  <a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT</a> objects.</div><div> </div>

## -struct-fields

### -field x

Unsigned 8-bit integer value in the range [0, 255] describing the x-coordinate of the vector.

### -field y

Unsigned 8-bit integer value in the range [0, 255] describing the y-coordinate of the vector.

### -field v

### -field XMUBYTE2

TBD

### -field operator=

TBD

## -remarks

You can use <a href="/windows/desktop/api/directxpackedvector/nf-directxpackedvector-xmloadubyte2">XMLoadUByte2</a> to load <code>XMUBYTE2</code> 
     into instances of <a href="/windows/desktop/dxmath/xmvector-data-type">XMVECTOR</a>.

You can use <a href="/windows/desktop/api/directxpackedvector/nf-directxpackedvector-xmstoreubyte2">XMStoreUByte2</a> to store instances of <code>XMVECTOR</code> 
   into an instance of <code>XMUBYTE2</code>.

<b>Namespace:</b> Use DirectX::PackedVector

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-structures">DirectXMath Library Structures</a>



<a href="/windows/desktop/dxmath/ovw-xmubyte2-extensions">XMUBYTE2 Extensions</a>