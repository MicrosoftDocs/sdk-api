---
UID: NS:directxpackedvector.XMUBYTE4
title: XMUBYTE4
author: windows-sdk-content
description: Describes a 4D vector where each component is a unsigned integer, 8-bits (1 byte) in length.
old-location: dxmath\xmubyte4.htm
tech.root: dxmath
ms.assetid: T:Microsoft.directx_sdk.reference.XMUBYTE4
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: XMUBYTE4, XMUBYTE4 structure [DirectX Math Support APIs], directxpackedvector/XMUBYTE4, dxmath.xmubyte4
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - XMUBYTE4
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# XMUBYTE4 structure


## -description


Describes a 4D vector where each component is a unsigned integer, 8-bits (1 byte) in length.
    

A 4D vector where each component is a unsigned integer, 8-bits (1 byte) in length.
    



For a list of additional functionality such as constructors and operators that are available
	using <code>XMUBYTE4</code> when you are programming in C++, see <a href="https://msdn.microsoft.com/d606293a-3a6d-49b5-832c-82ee5943c634">XMUBYTE4 Extensions</a>.
<div class="alert"><b>Note</b>  See <a href="https://msdn.microsoft.com/31512657-c413-9e6e-e343-1ea677a02b8c">DirectXMath Library Type
	Equivalences</a> for information about equivalent <a href="https://msdn.microsoft.com/993fc7e4-4752-4bce-82d0-0a034fdc69c0">D3DDECLTYPE</a>, <a href="https://msdn.microsoft.com/a222e3bb-310c-4019-93ee-6a2da2a46ded">D3DFORMAT</a>, and <a href="https://msdn.microsoft.com/dce61bc4-4ed5-4e64-84e8-6db88025e5c2">DXGI_FORMAT</a> objects.
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

Unsigned 32-bit 8-bit integer representing the 4D vector.
		    


## -remarks



<code>XMUBYTE4</code> can be loaded into instances of <a href="https://msdn.microsoft.com/1a044094-444d-e787-fa6a-76e88531aef1">XMVECTOR</a> by using
	    <a href="https://msdn.microsoft.com/55718879-5536-497e-a03e-1e66450f3517">XMLoadUByte4</a>.
	

Instances of <code>XMVECTOR</code> can be stored into an instance of <code>XMUBYTE4</code> with <a href="https://msdn.microsoft.com/8b6bc255-6eee-42bd-b4fb-da9ca9746c84">XMStoreUByte4</a>.
	

<b>Namespace:</b> Use DirectX::PackedVector

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/58acb05d-e79b-8f42-4cf4-76ae57929739">DirectXMath Library Structures</a>



<a href="https://msdn.microsoft.com/d606293a-3a6d-49b5-832c-82ee5943c634">XMUBYTE4 Extensions</a>
 

 

