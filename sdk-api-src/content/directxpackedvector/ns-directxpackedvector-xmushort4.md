---
UID: NS:directxpackedvector.XMUSHORT4
title: XMUSHORT4 (directxpackedvector.h)
description: A 4D vector consisting of 16-bit unsigned integer components.
helpviewer_keywords: ["XMUSHORT4","XMUSHORT4 structure [DirectX Math Support APIs]","directxpackedvector/XMUSHORT4","dxmath.xmushort4"]
old-location: dxmath\xmushort4.htm
tech.root: dxmath
ms.assetid: T:Microsoft.directx_sdk.reference.XMUSHORT4
ms.date: 12/05/2018
ms.keywords: XMUSHORT4, XMUSHORT4 structure [DirectX Math Support APIs], directxpackedvector/XMUSHORT4, dxmath.xmushort4
f1_keywords:
- directxpackedvector/XMUSHORT4
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
- XMUSHORT4
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# XMUSHORT4 structure


## -description


A 4D vector consisting of 16-bit unsigned integer components.
    



For a list of additional functionality such as constructors and operators that are available
	using <code>XMUSHORT4</code> when you are programming in C++, see <a href="https://docs.microsoft.com/windows/desktop/dxmath/ovw-xmushort4-extensions">XMUSHORT4 Extensions</a>.
<div class="alert"><b>Note</b>  See <a href="https://docs.microsoft.com/windows/desktop/dxmath/pg-xnamath-internals">DirectXMath Library Type
	Equivalences</a> for information about equivalent <a href="https://docs.microsoft.com/windows/desktop/direct3d9/d3ddecltype">D3DDECLTYPE</a>, <a href="https://docs.microsoft.com/windows/desktop/direct3d9/d3dformat">D3DFORMAT</a>, and <a href="https://docs.microsoft.com/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT</a> objects.
    </div><div> </div>

## -struct-fields




### -field x

Unsigned 16-bit integer in the range [0, 65535] describing the x-coordinate of the
		    vector.
		


### -field y

Unsigned 16-bit integer in the range [0, 65535] describing the y-coordinate of the
		    vector.
		


### -field z

Unsigned 16-bit integer in the range [0, 65535] describing the z-coordinate of the
		    vector.
		


### -field w

Unsigned 16-bit integer in the range [0, 65535] describing the w-coordinate of the
		    vector.
		


### -field v

 


### -field XMUSHORT4

TBD 


### -field operator=

TBD 




## -remarks



<code>XMUSHORT4</code> can be loaded into instances of <a href="https://docs.microsoft.com/windows/desktop/dxmath/xmvector-data-type"> XMVECTOR</a> by
	    using <a href="https://docs.microsoft.com/windows/desktop/api/directxpackedvector/nf-directxpackedvector-xmloadushort4">XMLoadUShort4</a>.
	

Instances of <code>XMVECTOR</code> can be stored into an instance of <code>XMUSHORT4</code> with <a href="https://docs.microsoft.com/windows/desktop/api/directxpackedvector/nf-directxpackedvector-xmstoreushort4">XMStoreUShort4</a>.
	

<b>Namespace:</b> Use DirectX::PackedVector

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/dxmath/ovw-xnamath-reference-structures">DirectXMath Library Structures</a>



<a href="https://docs.microsoft.com/windows/desktop/dxmath/ovw-xmushort4-extensions">XMUSHORT4 Extensions</a>
 

 

