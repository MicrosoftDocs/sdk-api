---
UID: NS:directxpackedvector.XMDECN4
title: XMDECN4 (directxpackedvector.h)
description: A 4D vector for storing signed, normalized values as 10 bit signed x-,y-, and z- components and a 2 bit signed w-component.
helpviewer_keywords: ["XMDECN4","XMDECN4 structure [DirectX Math Support APIs]","directxpackedvector/XMDECN4","dxmath.xmdecn4"]
old-location: dxmath\xmdecn4.htm
tech.root: dxmath
ms.assetid: T:Microsoft.directx_sdk.reference.XMDECN4
ms.date: 12/05/2018
ms.keywords: XMDECN4, XMDECN4 structure [DirectX Math Support APIs], directxpackedvector/XMDECN4, dxmath.xmdecn4
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
 - XMDECN4
 - directxpackedvector/XMDECN4
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
 - XMDECN4
---

# XMDECN4 structure


## -description

A 4D vector for storing signed, normalized values as 10 bit signed x-,y-, and z- components
      and a 2 bit signed w-component.
  



For a list of additional functionality such as constructors and operators that are available
	using <code>XMDECN4</code> when you are programming in C++, see <a href="/windows/desktop/dxmath/ovw-xmdecn4-extensions">XMDECN4 Extensions</a>.
<div class="alert"><b>Note</b>  See <a href="/windows/desktop/dxmath/pg-xnamath-internals">DirectXMath Library Type
	Equivalences</a> for information about equivalent <a href="/windows/desktop/direct3d9/d3ddecltype">D3DDECLTYPE</a>, <a href="/windows/desktop/direct3d9/d3dformat">D3DFORMAT</a>,and <a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT</a> objects.
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

Signed integer value in the range [-1, 1] describing the
			    w-coordinate of the vector.

### -field v

Unsigned 32-bit integer representing the 4D vector.

### -field XMDECN4

TBD

### -field operator uint32_t

TBD

### -field operator=

TBD

## -remarks

Those <code>XMDECN4</code> constructors using floating point arguments require normalized input,
	    which must be in the range of [-1.0.-1.0]. During instantiation, the inputs
	    specifying the x-, y-, and z-components are then multiplied by 511.0f, the results are
	    rounded and then assigned to the appropriate members of <code>XMDECN4</code>.
      

<code>XMDECN4</code> can be used to load instances of <a href="/windows/desktop/dxmath/xmvector-data-type">XMVECTOR</a> from
	  normalized values, by using <a href="/windows/desktop/api/directxpackedvector/nf-directxpackedvector-xmloaddecn4">XMLoadDecN4</a>, which divides the x-, y-, and
	  z-components by 511.0f, rounds the result, and then assigns the components to
	  an <code>XMVECTOR</code> instance.
      

<code>XMVECTOR</code> instances containing normalized values can be stored into <code>XMDECN4</code> using <a href="/windows/desktop/api/directxpackedvector/nf-directxpackedvector-xmstoredecn4">XMStoreDecN4</a>, which multiplies the x-, y-,and z-components by
	  511.0f , rounding the result, before assigning the values to the appropriate <code>XMDECN4</code> members.
      

<b>Namespace:</b> Use DirectX::PackedVector

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-structures">DirectXMath Library Structures</a>



<a href="/windows/desktop/dxmath/ovw-xmdecn4-extensions">XMDECN4 Extensions</a>