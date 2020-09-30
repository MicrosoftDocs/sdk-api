---
UID: NS:directxpackedvector.XMUBYTE4
title: XMUBYTE4 (directxpackedvector.h)
description: Describes a 4D vector where each component is a unsigned integer, 8-bits (1 byte) in length.
helpviewer_keywords: ["XMUBYTE4","XMUBYTE4 structure [DirectX Math Support APIs]","directxpackedvector/XMUBYTE4","dxmath.xmubyte4"]
old-location: dxmath\xmubyte4.htm
tech.root: dxmath
ms.assetid: T:Microsoft.directx_sdk.reference.XMUBYTE4
ms.date: 12/05/2018
ms.keywords: XMUBYTE4, XMUBYTE4 structure [DirectX Math Support APIs], directxpackedvector/XMUBYTE4, dxmath.xmubyte4
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
 - XMUBYTE4
 - directxpackedvector/XMUBYTE4
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
 - XMUBYTE4
---

# XMUBYTE4 structure


## -description

Describes a 4D vector where each component is a unsigned integer, 8-bits (1 byte) in length.
    

A 4D vector where each component is a unsigned integer, 8-bits (1 byte) in length.
    



For a list of additional functionality such as constructors and operators that are available
	using <code>XMUBYTE4</code> when you are programming in C++, see <a href="/windows/desktop/dxmath/ovw-xmubyte4-extensions">XMUBYTE4 Extensions</a>.
<div class="alert"><b>Note</b>  See <a href="/windows/desktop/dxmath/pg-xnamath-internals">DirectXMath Library Type
	Equivalences</a> for information about equivalent <a href="/windows/desktop/direct3d9/d3ddecltype">D3DDECLTYPE</a>, <a href="/windows/desktop/direct3d9/d3dformat">D3DFORMAT</a>, and <a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT</a> objects.
    </div><div> </div>

## -struct-fields

### -field x

Unsigned 8-bit integer value in the range [0, 255] describing the x-coordinate
			    of the vector.

### -field y

Unsigned 8-bit integer value in the range [0, 255] describing the y-coordinate
			    of the vector.

### -field z

Unsigned 8-bit integer value in the range [0, 255] describing the z-coordinate
			    of the vector.

### -field w

Unsigned 8-bit integer value in the range [0, 255] describing the w-coordinate
			    of the vector.

### -field v

Unsigned 32-bit 8-bit integer representing the 4D vector.

### -field XMUBYTE4

TBD

### -field operator=

TBD

## -remarks

<code>XMUBYTE4</code> can be loaded into instances of <a href="/windows/desktop/dxmath/xmvector-data-type">XMVECTOR</a> by using
	    <a href="/windows/desktop/api/directxpackedvector/nf-directxpackedvector-xmloadubyte4">XMLoadUByte4</a>.
	

Instances of <code>XMVECTOR</code> can be stored into an instance of <code>XMUBYTE4</code> with <a href="/windows/desktop/api/directxpackedvector/nf-directxpackedvector-xmstoreubyte4">XMStoreUByte4</a>.
	

<b>Namespace:</b> Use DirectX::PackedVector

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-structures">DirectXMath Library Structures</a>



<a href="/windows/desktop/dxmath/ovw-xmubyte4-extensions">XMUBYTE4 Extensions</a>