---
UID: NS:directxpackedvector.XMUSHORT2
title: XMUSHORT2
author: windows-sdk-content
description: Describes a 2D vector consisting of 16-bit unsigned integer components.
old-location: dxmath\xmushort2.htm
tech.root: dxmath
ms.assetid: T:Microsoft.directx_sdk.reference.XMUSHORT2
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: XMUSHORT2, XMUSHORT2 structure [DirectX Math Support APIs], directxpackedvector/XMUSHORT2, dxmath.xmushort2
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
 - XMUSHORT2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# XMUSHORT2 structure


## -description


Describes a 2D vector consisting of 16-bit unsigned integer components.
    



For a list of additional functionality such as constructors and operators that are available
	using <code>XMUSHORT2</code> when you are programming in C++, see <a href="https://msdn.microsoft.com/20e1c812-2c0b-483e-a9fd-e4188b04a024">XMUSHORT2 Extensions</a>.
<div class="alert"><b>Note</b>  See <a href="https://msdn.microsoft.com/31512657-c413-9e6e-e343-1ea677a02b8c">DirectXMath Library Type
	Equivalences</a> for information about equivalent <a href="https://msdn.microsoft.com/993fc7e4-4752-4bce-82d0-0a034fdc69c0">D3DDECLTYPE</a>, <a href="https://msdn.microsoft.com/a222e3bb-310c-4019-93ee-6a2da2a46ded">D3DFORMAT</a>, and <a href="https://msdn.microsoft.com/dce61bc4-4ed5-4e64-84e8-6db88025e5c2">DXGI_FORMAT</a> objects.
    </div><div> </div>

## -struct-fields




### -field x

Unsigned integer in the range [0, 65535] describing the x-coordinate of the
		    vector.
		


### -field y

Unsigned integer in the range [0, 65535] describing the y-coordinate of the
		    vector.
		


### -field v

 


### -field XMUSHORT2

TBD 


### -field operator=

TBD 




## -remarks



<code>XMUSHORT2</code> can be loaded into instances of <a href="https://msdn.microsoft.com/1a044094-444d-e787-fa6a-76e88531aef1">XMVECTOR</a> by using
	    <a href="https://msdn.microsoft.com/0404d49b-9bb8-43e7-8874-10612d5e54bf">XMLoadUShort2</a>.
	

Instances of <code>XMVECTOR</code> can be stored into an instance of <code>XMUSHORT2</code> with <a href="https://msdn.microsoft.com/b0b32dc8-4eb3-422e-9073-9cb607422831">XMStoreUShort2</a>.
	

<b>Namespace:</b> Use DirectX::PackedVector

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/58acb05d-e79b-8f42-4cf4-76ae57929739">DirectXMath Library Structures</a>



<a href="https://msdn.microsoft.com/20e1c812-2c0b-483e-a9fd-e4188b04a024">XMUSHORT2 Extensions</a>
 

 

