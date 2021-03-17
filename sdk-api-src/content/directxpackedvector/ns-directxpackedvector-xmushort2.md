---
UID: NS:directxpackedvector.XMUSHORT2
title: XMUSHORT2 (directxpackedvector.h)
description: Describes a 2D vector consisting of 16-bit unsigned integer components.
helpviewer_keywords: ["XMUSHORT2","XMUSHORT2 structure [DirectX Math Support APIs]","directxpackedvector/XMUSHORT2","dxmath.xmushort2"]
old-location: dxmath\xmushort2.htm
tech.root: dxmath
ms.assetid: T:Microsoft.directx_sdk.reference.XMUSHORT2
ms.date: 12/05/2018
ms.keywords: XMUSHORT2, XMUSHORT2 structure [DirectX Math Support APIs], directxpackedvector/XMUSHORT2, dxmath.xmushort2
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
 - XMUSHORT2
 - directxpackedvector/XMUSHORT2
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
 - XMUSHORT2
---

# XMUSHORT2 structure


## -description

Describes a 2D vector consisting of 16-bit unsigned integer components.
    



For a list of additional functionality such as constructors and operators that are available
	using <code>XMUSHORT2</code> when you are programming in C++, see <a href="/windows/desktop/dxmath/ovw-xmushort2-extensions">XMUSHORT2 Extensions</a>.
<div class="alert"><b>Note</b>  See <a href="/windows/desktop/dxmath/pg-xnamath-internals">DirectXMath Library Type
	Equivalences</a> for information about equivalent <a href="/windows/desktop/direct3d9/d3ddecltype">D3DDECLTYPE</a>, <a href="/windows/desktop/direct3d9/d3dformat">D3DFORMAT</a>, and <a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT</a> objects.
    </div><div> </div>

## -struct-fields

### -field x

Unsigned integer in the range [0, 65535] describing the x-coordinate of the
		    vector.

### -field y

Unsigned integer in the range [0, 65535] describing the y-coordinate of the
		    vector.

### -field v

### -field XMUSHORT2

TBD

### -field operator=

TBD

## -remarks

<code>XMUSHORT2</code> can be loaded into instances of <a href="/windows/desktop/dxmath/xmvector-data-type">XMVECTOR</a> by using
	    <a href="/windows/desktop/api/directxpackedvector/nf-directxpackedvector-xmloadushort2">XMLoadUShort2</a>.
	

Instances of <code>XMVECTOR</code> can be stored into an instance of <code>XMUSHORT2</code> with <a href="/windows/desktop/api/directxpackedvector/nf-directxpackedvector-xmstoreushort2">XMStoreUShort2</a>.
	

<b>Namespace:</b> Use DirectX::PackedVector

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-structures">DirectXMath Library Structures</a>



<a href="/windows/desktop/dxmath/ovw-xmushort2-extensions">XMUSHORT2 Extensions</a>