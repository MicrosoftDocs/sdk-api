---
UID: NS:directxpackedvector.XMXDEC4
title: XMXDEC4 (directxpackedvector.h)
description: A 4D vector with x-,y-, and z- components represented as 10 bit signed integer values, and the w-component as a 2 bit unsigned integer value.
helpviewer_keywords: ["XMXDEC4","XMXDEC4 structure [DirectX Math Support APIs]","directxpackedvector/XMXDEC4","dxmath.xmxdec4"]
old-location: dxmath\xmxdec4.htm
tech.root: dxmath
ms.assetid: T:Microsoft.directx_sdk.reference.XMXDEC4
ms.date: 12/05/2018
ms.keywords: XMXDEC4, XMXDEC4 structure [DirectX Math Support APIs], directxpackedvector/XMXDEC4, dxmath.xmxdec4
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
 - XMXDEC4
 - directxpackedvector/XMXDEC4
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
 - XMXDEC4
---

# XMXDEC4 structure


## -description

A 4D vector with x-,y-, and z- components represented as 10 bit signed integer values, and the
	w-component as a 2 bit unsigned integer value.
<div class="alert"><b>Note</b>  See <a href="/windows/desktop/dxmath/pg-xnamath-internals">DirectXMath Library Type
	Equivalences</a> for information about equivalent <a href="/windows/desktop/direct3d9/d3ddecltype">D3DDECLTYPE</a>, <a href="/windows/desktop/direct3d9/d3dformat">D3DFORMAT</a>, and <a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT</a> objects.
    </div><div> </div>

## -struct-fields

### -field x

Signed integer value in the range [-511, 511] describing the
			    x-coordinate of the vector.

### -field y

Signed integer value in the range [-511, 511] describing the
			    y-coordinate of the vector.

### -field z

Signed integer value in the range [-511, 511] describing the
			    z-coordinate of the vector.

### -field w

Unsigned integer value in the range [0, 3] describing the w-coordinate
			    of the vector.

### -field v

Unsigned 32-bit integer representing the 4D vector.

### -field XMXDEC4

TBD

### -field operator uint32_t

TBD

### -field operator=

TBD

## -remarks

<code>XMXDEC4</code> can be loaded into instances of <a href="/windows/desktop/dxmath/xmvector-data-type">XMVECTOR</a> by using
	    <a href="/windows/desktop/api/directxpackedvector/nf-directxpackedvector-xmloadxdec4">XMLoadXDec4</a>.
	

Instances of <code>XMVECTOR</code> can be stored into an instance of <code>XMXDEC4</code> with <a href="/windows/desktop/api/directxpackedvector/nf-directxpackedvector-xmstorexdec4">XMStoreXDec4</a>.
	

<b>Namespace:</b> Use DirectX::PackedVector

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-structures">DirectXMath Library Structures</a>



<a href="/windows/desktop/dxmath/ovw-xmxdec4-extensions">XMXDEC4 Extensions</a>