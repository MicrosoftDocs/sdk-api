---
UID: NS:directxpackedvector.XMCOLOR
title: XMCOLOR
author: windows-sdk-content
description: A 32-bit Alpha Red Green Blue (ARGB) color vector, where each color channel is specified as an unsigned 8 bit integer.
old-location: dxmath\xmcolor.htm
old-project: dxmath
ms.assetid: T:Microsoft.directx_sdk.reference.XMCOLOR
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: XMCOLOR, XMCOLOR structure [DirectX Math Support APIs], directxpackedvector/XMCOLOR, dxmath.xmcolor
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
req.namespace: DirectX::PackedVector
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - DirectXPackedVector.h
api_name:
 - XMCOLOR
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# XMCOLOR structure


## -description


A 32-bit Alpha Red Green Blue (ARGB) color vector, where each color channel is specified as
	an unsigned 8 bit integer.



For a list of additional functionality such as constructors and operators that are available
	using <code>XMCOLOR</code> when you are programming in C++, see <a href="https://msdn.microsoft.com/c2bf32a8-deb8-4aec-a94e-98d437c315f6">XMCOLOR Extensions</a>.
<div class="alert"><b>Note</b>  See <a href="https://msdn.microsoft.com/31512657-c413-9e6e-e343-1ea677a02b8c">DirectXMath Library Type
	Equivalences</a> for information about equivalent <a href="https://msdn.microsoft.com/993fc7e4-4752-4bce-82d0-0a034fdc69c0">D3DDECLTYPE</a>, 
  <a href="https://msdn.microsoft.com/a222e3bb-310c-4019-93ee-6a2da2a46ded">D3DFORMAT</a>,and <a href="https://msdn.microsoft.com/dce61bc4-4ed5-4e64-84e8-6db88025e5c2">DXGI_FORMAT</a> objects.</div><div> </div>

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


## -remarks



Those <code>XMCOLOR</code> constructors using floating point arguments require normalized input, which
	    are clamped to the range of [0-1.0].  During instantiation, the floating point data
	    specifying the color channels are multiplied by 255.0f, rounded and then assigned to the
	    appropriate members of <code>XMCOLOR</code>.

<code>XMCOLOR</code> can be used to load instances of <a href="https://msdn.microsoft.com/1a044094-444d-e787-fa6a-76e88531aef1"> XMVECTOR</a> from
	    normalized values, by using <a href="https://msdn.microsoft.com/beca676b-ca6b-42c5-8913-439c13224c8d">XMLoadColor</a>, which divides color channel
	    data by 255.0f, rounds the result, and then assigns the components to an <code>XMVECTOR</code>instance.

<code>XMVECTOR</code> instances containing normalized values can be stored into <code>XMCOLOR</code>using <a href="https://msdn.microsoft.com/4ea82b90-1eb2-4684-966e-0d48289a790f">XMStoreColor</a>, which multiplies color channel data by 255.0f,
	    rounding the result before assigning the values to the appropriate <code>XMCOLOR</code> members.

<b>Namespace:</b> Use DirectX::PackedVector

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/58acb05d-e79b-8f42-4cf4-76ae57929739">DirectXMath Library Structures</a>



<a href="https://msdn.microsoft.com/c2bf32a8-deb8-4aec-a94e-98d437c315f6">XMCOLOR Extensions</a>
 

 

