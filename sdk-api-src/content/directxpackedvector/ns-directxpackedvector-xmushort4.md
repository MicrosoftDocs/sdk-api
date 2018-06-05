---
UID: NS:directxpackedvector.XMUSHORT4
title: XMUSHORT4
author: windows-sdk-content
description: A 4D vector consisting of 16-bit unsigned integer components.
old-location: dxmath\xmushort4.htm
old-project: dxmath
ms.assetid: T:Microsoft.directx_sdk.reference.XMUSHORT4
ms.author: windowssdkdev
ms.date: 04/23/2018
ms.keywords: XMUSHORT4, XMUSHORT4 structure [DirectX Math Support APIs], directxpackedvector/XMUSHORT4, dxmath.xmushort4
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
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	DirectXPackedVector.h
api_name:
-	XMUSHORT4
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# XMUSHORT4 structure


## -description



	A 4D vector consisting of 16-bit unsigned integer components.
    




	For a list of additional functionality such as constructors and operators that are available
	using <code>XMUSHORT4</code> when you are programming in C++, see <a href="https://msdn.microsoft.com/71c50c11-4be2-4d7d-ae53-0f3b95981998">XMUSHORT4 Extensions</a>.
<div class="alert"><b>Note</b>  
	See <a href="https://msdn.microsoft.com/31512657-c413-9e6e-e343-1ea677a02b8c">DirectXMath Library Type
	Equivalences</a> for information about equivalent <a href="https://msdn.microsoft.com/993fc7e4-4752-4bce-82d0-0a034fdc69c0">D3DDECLTYPE</a>, <a href="https://msdn.microsoft.com/a222e3bb-310c-4019-93ee-6a2da2a46ded">D3DFORMAT</a>, and <a href="https://msdn.microsoft.com/dce61bc4-4ed5-4e64-84e8-6db88025e5c2">DXGI_FORMAT</a> objects.
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

 




## -remarks



<code>XMUSHORT4</code> can be loaded into instances of <a href="https://msdn.microsoft.com/1a044094-444d-e787-fa6a-76e88531aef1"> XMVECTOR</a> by
	    using <a href="https://msdn.microsoft.com/87367099-9e73-44de-a045-a9fbbb396455">XMLoadUShort4</a>.
	


	    Instances of <code>XMVECTOR</code> can be stored into an instance of <code>XMUSHORT4</code> with <a href="https://msdn.microsoft.com/7d1db031-d336-4ee2-b1e7-5835bf2ca399">XMStoreUShort4</a>.
	

<b>Namespace:</b> Use DirectX::PackedVector

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/58acb05d-e79b-8f42-4cf4-76ae57929739">DirectXMath Library Structures</a>



<a href="https://msdn.microsoft.com/71c50c11-4be2-4d7d-ae53-0f3b95981998">XMUSHORT4 Extensions</a>
 

 

