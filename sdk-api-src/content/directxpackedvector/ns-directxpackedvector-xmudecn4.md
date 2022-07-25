---
UID: NS:directxpackedvector.XMUDECN4
title: XMUDECN4 (directxpackedvector.h)
description: A 4D vector for storing unsigned, normalized integer values as 10 bit unsigned x-, y-, and z-components and a 2-bit unsigned w-component.
helpviewer_keywords: ["XMUDECN4","XMUDECN4 structure [DirectX Math Support APIs]","directxpackedvector/XMUDECN4","dxmath.xmudecn4"]
old-location: dxmath\xmudecn4.htm
tech.root: dxmath
ms.assetid: T:Microsoft.directx_sdk.reference.XMUDECN4
ms.date: 12/05/2018
ms.keywords: XMUDECN4, XMUDECN4 structure [DirectX Math Support APIs], directxpackedvector/XMUDECN4, dxmath.xmudecn4
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
 - XMUDECN4
 - directxpackedvector/XMUDECN4
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
 - XMUDECN4
---

# XMUDECN4 structure


## -description

A 4D vector for storing unsigned, normalized integer values as 10 bit unsigned x-, y-, 
  and z-components and a 2-bit unsigned w-component.
    

For a list of more functionality such as constructors and operators that are available
	using <code>XMUDECN4</code> when you are programming in C++, see <a href="/windows/desktop/dxmath/ovw-xmudecn4-extensions">XMUDECN4 Extensions</a>.
<div class="alert"><b>Note</b>  See <a href="/windows/desktop/dxmath/pg-xnamath-internals">DirectXMath Library Type
	Equivalences</a> for information about equivalent <a href="/windows/desktop/direct3d9/d3ddecltype">D3DDECLTYPE</a>, <a href="/windows/desktop/direct3d9/d3dformat">D3DFORMAT</a>, and <a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT</a> objects.
    </div><div> </div>

## -struct-fields

### -field x

Unsigned integer value in the range [0, 1023] describing the
			    x-coordinate of the vector.

### -field y

Unsigned integer value in the range [0, 1023] describing the
			    y-coordinate of the vector.

### -field z

Unsigned integer value in the range [0, 1023] describing the
			    z-coordinate of the vector.

### -field w

Unsigned integer value in the range [0, 3] describing the w-coordinate
			    of the vector.

### -field v

Unsigned 32-bit integer representing the 4D vector.

### -field XMUDECN4

TBD

### -field operator uint32_t

TBD

### -field operator=

TBD

## -remarks

Those <code>XMUDECN4</code> constructors using floating point arguments require normalized input,
	    which must be in the range of [0.-1.0].  During instantiation, the inputs specifying the x-, y-,
	    and z-components are multiplied by 1023.0f, and the w-component are multiplied by 3.0f.
      The results are rounded, and then assigned to the appropriate members of <code>XMUDECN4</code>.
	

You can use <code>XMUDECN4</code> to load instances of <a href="/windows/desktop/dxmath/xmvector-data-type">XMVECTOR</a> from normalized values 
      by using <a href="/windows/desktop/api/directxpackedvector/nf-directxpackedvector-xmloadudecn4">XMLoadUDecN4</a>, which divides the x-, y-, and
	    z-components by 1023.0f, divides the w-component by 3.0f, rounds the result, and then assigns
	    the components to an <code>XMVECTOR</code> instance.
	

<code>XMVECTOR</code> instances containing normalized values can be stored into <code>XMUDECN4</code> using <a href="/windows/desktop/api/directxpackedvector/nf-directxpackedvector-xmstoreudecn4">XMStoreUDecN4</a>, which multiplies the x-, y-, and z-components by
	    1023.0f, multiplies the w-component by 3.0f, and rounds the result before assigning the values 
      to the appropriate <code>XMUDECN4</code> members.
	

<b>Namespace:</b> Use DirectX::PackedVector

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-structures">DirectXMath Library Structures</a>



<a href="/windows/desktop/dxmath/ovw-xmudecn4-extensions">XMUDECN4 Extensions</a>