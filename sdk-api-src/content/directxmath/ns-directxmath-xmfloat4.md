---
UID: NS:directxmath.XMFLOAT4
title: XMFLOAT4 (directxmath.h)
description: Describes a 4D vector consisting of four single-precision floating-point values.
helpviewer_keywords: ["XMFLOAT4","XMFLOAT4 structure [DirectX Math Support APIs]","directxmath/XMFLOAT4","dxmath.xmfloat4"]
old-location: dxmath\xmfloat4.htm
tech.root: dxmath
ms.assetid: T:Microsoft.directx_sdk.reference.XMFLOAT4
ms.date: 12/05/2018
ms.keywords: XMFLOAT4, XMFLOAT4 structure [DirectX Math Support APIs], directxmath/XMFLOAT4, dxmath.xmfloat4
f1_keywords:
- directxmath/XMFLOAT4
dev_langs:
- c++
req.header: directxmath.h
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
- DirectXMath.h
api_name:
- XMFLOAT4
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# XMFLOAT4 structure


## -description


Describes a 4D vector consisting of four single-precision floating-point values.
    



For a list of additional functionality such as constructors and operators that are available
	using <code>XMFLOAT4</code> when you are programming in C++, see <a href="https://docs.microsoft.com/windows/desktop/dxmath/ovw-xmfloat4-extensions">XMFLOAT4 Extensions</a>.
<div class="alert"><b>Note</b>  See <a href="https://docs.microsoft.com/windows/desktop/dxmath/pg-xnamath-internals">DirectXMath Library Type
	Equivalences</a> for information about equivalent <a href="https://docs.microsoft.com/windows/desktop/direct3d9/d3ddecltype">D3DDECLTYPE</a>, <a href="https://docs.microsoft.com/windows/desktop/direct3d9/d3dformat">D3DFORMAT</a>, and <a href="https://docs.microsoft.com/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT</a> objects.
    </div><div> </div>

## -struct-fields




### -field x

<b>float</b> value describing the x-coordinate of the vector.
		


### -field y

<b>float</b> value describing the y-coordinate of the vector.
		


### -field z

<b>float</b> value describing the z-coordinate of the vector.
		


### -field w

<b>float</b> value describing the w-coordinate of the vector.
		


### -field operator=

TBD 


### -field XMFLOAT4

TBD 




## -remarks



<code>XMFLOAT4</code> can be loaded into instances of <a href="https://docs.microsoft.com/windows/desktop/dxmath/xmvector-data-type">XMVECTOR</a> by using
	    <a href="https://docs.microsoft.com/windows/desktop/api/directxmath/nf-directxmath-xmloadfloat4">XMLoadFloat4</a>.
	

Instances of <code>XMVECTOR</code> can be stored into an instance of <code>XMFLOAT4</code> with <a href="https://docs.microsoft.com/windows/desktop/api/directxmath/nf-directxmath-xmstorefloat4">XMStoreFloat4</a>.
	

<b>Namespace:</b> Use DirectX

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/dxmath/ovw-xnamath-reference-structures">DirectXMath Library Structures</a>



<a href="https://docs.microsoft.com/windows/desktop/dxmath/ovw-xmfloat4-extensions">XMFLOAT4 Extensions</a>
 

 

