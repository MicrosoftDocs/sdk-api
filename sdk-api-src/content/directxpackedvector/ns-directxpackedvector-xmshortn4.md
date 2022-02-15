---
UID: NS:directxpackedvector.XMSHORTN4
title: XMSHORTN4 (directxpackedvector.h)
description: A 4D vector for storing signed, normalized values as signed 16-bit integers, (type int16_t).
helpviewer_keywords: ["XMSHORTN4","XMSHORTN4 structure [DirectX Math Support APIs]","directxpackedvector/XMSHORTN4","dxmath.xmshortn4"]
old-location: dxmath\xmshortn4.htm
tech.root: dxmath
ms.assetid: T:Microsoft.directx_sdk.reference.XMSHORTN4
ms.date: 12/05/2018
ms.keywords: XMSHORTN4, XMSHORTN4 structure [DirectX Math Support APIs], directxpackedvector/XMSHORTN4, dxmath.xmshortn4
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
 - XMSHORTN4
 - directxpackedvector/XMSHORTN4
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
 - XMSHORTN4
---

# XMSHORTN4 structure


## -description

A 4D vector for storing signed, normalized values as  signed 16-bit integers, (type <code>int16_t</code>).
    



For a list of additional functionality such as constructors and operators that are available
	using <code>XMSHORTN4</code> when you are programming in C++, see <a href="/windows/desktop/dxmath/ovw-xmshortn4-extensions">XMSHORTN4 Extensions</a>.
<div class="alert"><b>Note</b>  See <a href="/windows/desktop/dxmath/pg-xnamath-internals">DirectXMath Library Type
	Equivalences</a> for information about equivalent <a href="/windows/desktop/direct3d9/d3ddecltype">D3DDECLTYPE</a>, <a href="/windows/desktop/direct3d9/d3dformat">D3DFORMAT</a>, and <a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT</a> objects.
    </div><div> </div>

## -struct-fields

### -field x

Signed 16-bit integer in the range [-32767, 32767] describing the x-coordinate
		    of the vector.

### -field y

Signed 16-bit integer in the range [-32767, 32767] describing the y-coordinate
		    of the vector.

### -field z

Signed 16-bit integer in the range [-32767, 32767] describing the z-coordinate
		    of the vector.

### -field w

Signed 16-bit integer in the range [-32767, 32767] describing the w-coordinate
		    of the vector.

### -field v

### -field XMSHORTN4

TBD

### -field operator=

TBD

## -remarks

Those <code>XMSHORTN4</code> constructors using floating point arguments require normalized input,
	    which must be in the range of [-1.0.-1.0].  During instantiation, these data are
	    multiplied by 32767.0f, results are rounded, and then
	    assigned to the appropriate members of <code>XMSHORTN4</code>.

	

<code>XMSHORTN4</code> can be used to load instances of <a href="/windows/desktop/dxmath/xmvector-data-type">XMVECTOR</a> from
	    normalized values, by using <a href="/windows/desktop/api/directxpackedvector/nf-directxpackedvector-xmloadshortn4">XMLoadShortN4</a>, which divides each
	    component 32767.0f, rounds the result, and then assigns the components to an
	    <code>XMVECTOR</code> instance.
	

<code>XMVECTOR</code> instances containing normalized values can be stored into <code>XMSHORTN4</code> using <a href="/windows/desktop/api/directxpackedvector/nf-directxpackedvector-xmstoreshortn4">XMStoreShortN4</a>, which multiplies each component by 32767.0f,
	    rounding the result, before assigning the values to the appropriate <code>XMSHORTN4</code> members.
	

<b>Namespace:</b> Use DirectX::PackedVector

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-structures">DirectXMath Library Structures</a>



<a href="/windows/desktop/dxmath/ovw-xmshortn4-extensions">XMSHORTN4 Extensions</a>