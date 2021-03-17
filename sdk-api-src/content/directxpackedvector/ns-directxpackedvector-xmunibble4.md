---
UID: NS:directxpackedvector.XMUNIBBLE4
title: XMUNIBBLE4 (directxpackedvector.h)
description: A 4D vector with four unsigned 4-bit integer components.
helpviewer_keywords: ["XMUNIBBLE4","XMUNIBBLE4 structure [DirectX Math Support APIs]","directxpackedvector/XMUNIBBLE4","dxmath.xmunibble4"]
old-location: dxmath\xmunibble4.htm
tech.root: dxmath
ms.assetid: T:Microsoft.directx_sdk.reference.XMUNIBBLE4
ms.date: 12/05/2018
ms.keywords: XMUNIBBLE4, XMUNIBBLE4 structure [DirectX Math Support APIs], directxpackedvector/XMUNIBBLE4, dxmath.xmunibble4
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
 - XMUNIBBLE4
 - directxpackedvector/XMUNIBBLE4
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
 - XMUNIBBLE4
---

## -description

A 4D vector with four unsigned 4-bit integer components.

For a list of additional functionality such as constructors and operators that are available
	using <code>XMUNIBBLE4</code> when you are programming in C++, see <a href="/windows/desktop/dxmath/ovw-xmunibble4-extensions">XMUNIBBLE4 Extensions</a>.

## -struct-fields

### -field v

Unsigned short representing the 4D vector in a packed format.

### -field w : 4

Unsigned 4-bit integer value in the range [0,15] describing the
			    w-coordinate of the vector.  The 4-bit x component.

### -field x : 4

Unsigned 4-bit integer value in the range [0,15] describing the
			    x-coordinate of the vector.  The 4-bit x component.

### -field y : 4

Unsigned 4-bit integer value in the range [0,15] describing the
			    y-coordinate of the vector.  The 4-bit x component.

### -field z : 4

Unsigned 4-bit integer value in the range [0,15] describing the
			    z-coordinate of the vector.  The 4-bit x component.

## -remarks

<code>XMUNIBBLE4</code> can be loaded into instances of <a href="/windows/desktop/dxmath/xmvector-data-type">XMVECTOR</a> by using
	    <a href="/windows/desktop/api/directxpackedvector/nf-directxpackedvector-xmloadunibble4">XMLoadUNibble4</a>.
	

Instances of <code>XMVECTOR</code> can be stored into an instance of <code>XMUNIBBLE4</code> with <a href="/windows/desktop/api/directxpackedvector/nf-directxpackedvector-xmstoreunibble4">XMStoreUNibble4</a>.
	

<b>Namespace:</b> Use DirectX::PackedVector

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-structures">DirectXMath Library Structures</a>



<a href="/windows/desktop/dxmath/ovw-xmunibble4-extensions">XMUNIBBLE4 Extensions</a>