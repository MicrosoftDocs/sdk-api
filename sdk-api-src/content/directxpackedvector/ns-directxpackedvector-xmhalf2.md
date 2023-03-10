---
UID: NS:directxpackedvector.XMHALF2
title: XMHALF2 (directxpackedvector.h)
description: A 2D vector consisting of two half-precision (16bit) floating-point values.
helpviewer_keywords: ["XMHALF2","XMHALF2 structure [DirectX Math Support APIs]","directxpackedvector/XMHALF2","dxmath.xmhalf2"]
old-location: dxmath\xmhalf2.htm
tech.root: dxmath
ms.assetid: T:Microsoft.directx_sdk.reference.XMHALF2
ms.date: 12/05/2018
ms.keywords: XMHALF2, XMHALF2 structure [DirectX Math Support APIs], directxpackedvector/XMHALF2, dxmath.xmhalf2
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
 - XMHALF2
 - directxpackedvector/XMHALF2
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
 - XMHALF2
---

# XMHALF2 structure


## -description

A 2D vector consisting of two half-precision (16bit) floating-point values.
    



For a list of additional functionality such as constructors and operators that are available
	using <code>XMHALF2</code> when you are programming in C++, see <a href="/windows/desktop/dxmath/ovw-xmhalf2-extensions">XMHALF2 Extensions</a>.
<div class="alert"><b>Note</b>  See <a href="/windows/desktop/dxmath/pg-xnamath-internals">DirectXMath Library Type
	Equivalences</a> for information about equivalent <a href="/windows/desktop/direct3d9/d3ddecltype">D3DDECLTYPE</a>, <a href="/windows/desktop/direct3d9/d3dformat">D3DFORMAT</a>, and <a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT</a> objects.
    </div><div> </div>

## -struct-fields

### -field x

<b>HALF</b> value describing the x-coordinate.

### -field y

<b>HALF</b> value describing the y-coordinate.

### -field v

### -field XMHALF2

TBD

### -field operator=

TBD

## -remarks

The definition of the <code>HALF</code> type used under DirectXMath is consistent with the <a href="https://ieeexplore.ieee.org/xpl/freeabs_all.jsp?arnumber=4610935">IEEE
	    standard</a>, and consists of a sign bit, a 5 bit biased exponent, and a 10 bit
	    mantissa:
	


```

                    [15] SEEEEEMMMMMMMMMM [0]
	
```


<code>XMHALF2</code> can be loaded into instances of <a href="/windows/desktop/dxmath/xmvector-data-type">XMVECTOR</a> by using <a href="/windows/desktop/api/directxpackedvector/nf-directxpackedvector-xmloadhalf2">XMLoadHalf2</a>.
	

Instances of <code>XMVECTOR</code> can be stored into an instance of <code>XMHALF2</code> with <a href="/windows/desktop/api/directxpackedvector/nf-directxpackedvector-xmstorehalf2">XMStoreHalf2</a>.
	

<b>Namespace:</b> Use DirectX::PackedVector

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-structures">DirectXMath Library Structures</a>



<a href="/windows/desktop/dxmath/ovw-xmhalf2-extensions">XMHALF2 Extensions</a>