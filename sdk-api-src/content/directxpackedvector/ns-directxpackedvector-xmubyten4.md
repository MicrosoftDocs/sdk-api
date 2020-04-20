---
UID: NS:directxpackedvector.XMUBYTEN4
title: XMUBYTEN4 (directxpackedvector.h)
description: A 3D vector for storing unsigned, normalized values as signed 8-bits (1 byte) integers.helpviewer_keywords: ["XMUBYTEN4","XMUBYTEN4 structure [DirectX Math Support APIs]","directxpackedvector/XMUBYTEN4","dxmath.xmubyten4"]
old-location: dxmath\xmubyten4.htm
tech.root: dxmath
ms.assetid: T:Microsoft.directx_sdk.reference.XMUBYTEN4
ms.date: 12/05/2018
ms.keywords: XMUBYTEN4, XMUBYTEN4 structure [DirectX Math Support APIs], directxpackedvector/XMUBYTEN4, dxmath.xmubyten4
f1_keywords:
- directxpackedvector/XMUBYTEN4
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- DirectXPackedVector.h
api_name:
- XMUBYTEN4
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# XMUBYTEN4 structure


## -description


A 3D vector for storing unsigned, normalized values as signed 8-bits (1 byte) integers.
    

For a list of additional functionality such as constructors and operators that are available
	using <code>XMUBYTEN4</code> when you are programming in C++, see <a href="https://docs.microsoft.com/windows/desktop/dxmath/ovw-xmubyten4-extensions">XMUBYTEN4 Extensions</a>.
<div class="alert"><b>Note</b>  See <a href="https://docs.microsoft.com/windows/desktop/dxmath/pg-xnamath-internals">DirectXMath Library Type
	Equivalences</a> for information about equivalent <a href="https://docs.microsoft.com/windows/desktop/direct3d9/d3ddecltype">D3DDECLTYPE</a>, <a href="https://docs.microsoft.com/windows/desktop/direct3d9/d3dformat">D3DFORMAT</a>, and <a href="https://docs.microsoft.com/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT</a> objects.
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

Unsigned 32-bit integer representing the 4D vector.
		    


### -field XMUBYTEN4

TBD 


### -field operator=

TBD 




## -remarks



Those <code>XMUBYTEN4</code> constructors using floating point arguments require normalized input,
	    which must be in the range of [0.0.-1.0].  During instantiation, these data are
	    multiplied by 255.0f, results are rounded, and then
	    assigned to the appropriate members of <code>XMUBYTEN4</code>.

	

<code>XMUBYTEN4</code> can be used to load instances of <a href="https://docs.microsoft.com/windows/desktop/dxmath/xmvector-data-type">XMVECTOR</a> from
	    normalized values, by using <a href="https://docs.microsoft.com/windows/desktop/api/directxpackedvector/nf-directxpackedvector-xmloadubyten4">XMLoadUByteN4</a>, which divides each
	    component 255.0f, rounds the result, and then assigns the components to an
	    <code>XMVECTOR</code> instance.
	

<code>XMVECTOR</code> instances containing normalized values can be stored into <code>XMUBYTEN4</code>using <a href="https://docs.microsoft.com/windows/desktop/api/directxpackedvector/nf-directxpackedvector-xmstoreubyten4">XMStoreUByteN4</a>, which multiplies each component by 255.0f,
	    rounding the result, before assigning the values to the appropriate <code>XMUBYTEN4</code> members.
	

<b>Namespace:</b> Use DirectX::PackedVector

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/dxmath/ovw-xnamath-reference-structures">DirectXMath Library Structures</a>



<a href="https://docs.microsoft.com/windows/desktop/dxmath/ovw-xmubyten4-extensions">XMUBYTEN4 Extensions</a>
 

 

