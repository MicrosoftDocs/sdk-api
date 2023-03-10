---
UID: NS:directxpackedvector.XMSHORT2
title: XMSHORT2 (directxpackedvector.h)
description: Describes a 2D vector consisting of 16-bit signed and normalized integer components.
helpviewer_keywords: ["XMSHORT2","XMSHORT2 structure [DirectX Math Support APIs]","directxpackedvector/XMSHORT2","dxmath.xmshort2"]
old-location: dxmath\xmshort2.htm
tech.root: dxmath
ms.assetid: T:Microsoft.directx_sdk.reference.XMSHORT2
ms.date: 12/05/2018
ms.keywords: XMSHORT2, XMSHORT2 structure [DirectX Math Support APIs], directxpackedvector/XMSHORT2, dxmath.xmshort2
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
 - XMSHORT2
 - directxpackedvector/XMSHORT2
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
 - XMSHORT2
---

# XMSHORT2 structure


## -description

Describes a 2D vector consisting of 16-bit signed and normalized integer components.
    

For a list of additional functionality such as constructors and operators that are available
	using <code>XMSHORT2</code> when you are programming in C++, see <a href="/windows/desktop/dxmath/ovw-xmshort2-extensions">XMSHORT2 Extensions</a>.
<div class="alert"><b>Note</b>  See <a href="/windows/desktop/dxmath/pg-xnamath-internals">DirectXMath Library Type
	Equivalences</a> for information about equivalent <a href="/windows/desktop/direct3d9/d3ddecltype">D3DDECLTYPE</a>, <a href="/windows/desktop/direct3d9/d3dformat">D3DFORMAT</a>, and <a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT</a> objects.
    </div><div> </div>

## -struct-fields

### -field x

Signed integer in the range [-32767, 32767] describing the x-coordinate
		    of the vector.

### -field y

Signed integer in the range [-32767, 32767] describing the y-coordinate
		    of the vector.

### -field v

### -field XMSHORT2

TBD

### -field operator=

TBD

## -remarks

The components are normalized when this structure is loaded into an <a href="/windows/desktop/dxmath/xmvector-data-type">XMVECTOR</a> using <a href="/windows/desktop/api/directxpackedvector/nf-directxpackedvector-xmloadshort2">XMLoadShort2</a>. Each component will be divided by 32767.0f.
	

<b>Namespace:</b> Use DirectX::PackedVector

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-structures">DirectXMath Library Structures</a>



<a href="/windows/desktop/dxmath/ovw-xmshort2-extensions">XMSHORT2 Extensions</a>