---
UID: NS:directxpackedvector.XMCOLOR
title: XMCOLOR (directxpackedvector.h)
description: A 32-bit Alpha Red Green Blue (ARGB) color vector, where each color channel is specified as an unsigned 8 bit integer.
helpviewer_keywords: ["XMCOLOR","XMCOLOR structure [DirectX Math Support APIs]","directxpackedvector/XMCOLOR","dxmath.xmcolor"]
old-location: dxmath\xmcolor.htm
tech.root: dxmath
ms.assetid: T:Microsoft.directx_sdk.reference.XMCOLOR
ms.date: 12/05/2018
ms.keywords: XMCOLOR, XMCOLOR structure [DirectX Math Support APIs], directxpackedvector/XMCOLOR, dxmath.xmcolor
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
 - XMCOLOR
 - directxpackedvector/XMCOLOR
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
 - XMCOLOR
---

# XMCOLOR structure


## -description

A 32-bit Alpha Red Green Blue (ARGB) color vector, where each color channel is specified as
	an unsigned 8 bit integer.



For a list of additional functionality such as constructors and operators that are available
	using <code>XMCOLOR</code> when you are programming in C++, see <a href="/windows/desktop/dxmath/ovw-xmcolor-extensions">XMCOLOR Extensions</a>.
<div class="alert"><b>Note</b>  See <a href="/windows/desktop/dxmath/pg-xnamath-internals">DirectXMath Library Type
	Equivalences</a> for information about equivalent <a href="/windows/desktop/direct3d9/d3ddecltype">D3DDECLTYPE</a>, 
  <a href="/windows/desktop/direct3d9/d3dformat">D3DFORMAT</a>,and <a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT</a> objects.</div><div> </div>

## -struct-fields

### -field b

Unsigned integer between 0 and 255 representing the blue component.

### -field g

Unsigned integer between 0 and 255 representing the green component.

### -field r

Unsigned integer between 0 and 255 representing the red component.

### -field a

Unsigned integer between 0 and 255 representing the alpha component.

### -field c

Unsigned 32-bit integer representing the color. The colors are stored in A8R8G8B8 format.

The alpha component the most-significant bits, and the blue component is
			    stored in the least-significant bits.

### -field XMCOLOR

TBD

### -field operator uint32_t

TBD

### -field operator=

TBD

## -remarks

Those <code>XMCOLOR</code> constructors using floating point arguments require normalized input, which
	    are clamped to the range of [0-1.0].  During instantiation, the floating point data
	    specifying the color channels are multiplied by 255.0f, rounded and then assigned to the
	    appropriate members of <code>XMCOLOR</code>.

<code>XMCOLOR</code> can be used to load instances of <a href="/windows/desktop/dxmath/xmvector-data-type"> XMVECTOR</a> from
	    normalized values, by using <a href="/windows/desktop/api/directxpackedvector/nf-directxpackedvector-xmloadcolor">XMLoadColor</a>, which divides color channel
	    data by 255.0f, rounds the result, and then assigns the components to an <code>XMVECTOR</code> instance.

<code>XMVECTOR</code> instances containing normalized values can be stored into <code>XMCOLOR</code> using <a href="/windows/desktop/api/directxpackedvector/nf-directxpackedvector-xmstorecolor">XMStoreColor</a>, which multiplies color channel data by 255.0f,
	    rounding the result before assigning the values to the appropriate <code>XMCOLOR</code> members.

<b>Namespace:</b> Use DirectX::PackedVector

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-structures">DirectXMath Library Structures</a>



<a href="/windows/desktop/dxmath/ovw-xmcolor-extensions">XMCOLOR Extensions</a>