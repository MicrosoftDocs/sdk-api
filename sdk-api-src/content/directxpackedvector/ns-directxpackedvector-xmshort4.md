---
UID: NS:directxpackedvector.XMSHORT4
title: XMSHORT4 (directxpackedvector.h)
description: A 4D vector consisting of 16-bit signed integer components.
helpviewer_keywords: ["XMSHORT4","XMSHORT4 structure [DirectX Math Support APIs]","directxpackedvector/XMSHORT4","dxmath.xmshort4"]
old-location: dxmath\xmshort4.htm
tech.root: dxmath
ms.assetid: T:Microsoft.directx_sdk.reference.XMSHORT4
ms.date: 12/05/2018
ms.keywords: XMSHORT4, XMSHORT4 structure [DirectX Math Support APIs], directxpackedvector/XMSHORT4, dxmath.xmshort4
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
 - XMSHORT4
 - directxpackedvector/XMSHORT4
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
 - XMSHORT4
---

# XMSHORT4 structure


## -description

A 4D vector consisting of 16-bit signed integer components.
    



For a list of additional functionality such as constructors and operators that are available
	using <code>XMSHORT4</code> when you are programming in C++, see <a href="/windows/desktop/dxmath/ovw-xmshort4-extensions">XMSHORT4 Extensions</a>.
<div class="alert"><b>Note</b>  See <a href="/windows/desktop/dxmath/pg-xnamath-internals">DirectXMath Library Type
	Equivalences</a> for information about equivalent <a href="/windows/desktop/direct3d9/d3ddecltype">D3DDECLTYPE</a>, <a href="/windows/desktop/direct3d9/d3dformat">D3DFORMAT</a>, and <a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT</a> objects.
    </div><div> </div>

## -struct-fields

### -field x

Signed 16-bit integer in the range [-32767, 32767] describing the
		    x-coordinate of the vector.

### -field y

Signed 16-bit integer in the range [-32767, 32767] describing the
		    y-coordinate of the vector.

### -field z

Signed 16-bit integer in the range [-32767, 32767] describing the
		    z-coordinate of the vector.

### -field w

Signed 16-bit integer in the range [-32767, 32767] describing the
		    w-coordinate of the vector.

### -field v

### -field XMSHORT4

TBD

### -field operator=

TBD

## -remarks

<code>XMSHORT4</code> can be loaded into instances of <a href="/windows/desktop/dxmath/xmvector-data-type"> XMVECTOR</a> by
	    using <a href="/windows/desktop/api/directxpackedvector/nf-directxpackedvector-xmloadshort4">XMLoadShort4</a>.
	

Instances of <code>XMVECTOR</code> can be stored into an instance of <code>XMSHORT4</code> with <a href="/windows/desktop/api/directxpackedvector/nf-directxpackedvector-xmstoreshort4">XMStoreShort4</a>.
	

<b>Namespace:</b> Use DirectX::PackedVector

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-structures">DirectXMath Library Structures</a>



<a href="/windows/desktop/dxmath/ovw-xmshort4-extensions">XMSHORT4 Extensions</a>