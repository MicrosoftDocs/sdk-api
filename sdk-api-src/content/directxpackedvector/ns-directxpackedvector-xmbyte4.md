---
UID: NS:directxpackedvector.XMBYTE4
title: XMBYTE4
author: windows-sdk-content
description: A 4D vector where each component is a signed integer, 8-bits (1 byte) in length.
old-location: dxmath\xmbyte4.htm
tech.root: dxmath
ms.assetid: T:Microsoft.directx_sdk.reference.XMBYTE4
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: XMBYTE4, XMBYTE4 structure [DirectX Math Support APIs], directxpackedvector/XMBYTE4, dxmath.xmbyte4
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
 - XMBYTE4
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# XMBYTE4 structure


## -description


A 4D vector where each component is a signed integer, 8-bits (1 byte) in length.
    

For a list of additional functionality such as constructors and operators that are available
	using <code>XMBYTE4</code> when you are programming in C++, see <a href="https://msdn.microsoft.com/en-us/library/Ee415259(v=VS.85).aspx">XMBYTE4 Extensions</a>.
<div class="alert"><b>Note</b>  See <a href="https://msdn.microsoft.com/31512657-c413-9e6e-e343-1ea677a02b8c">DirectXMath Library Type
	Equivalences</a> for information about equivalent <a href="https://msdn.microsoft.com/en-us/library/Bb172533(v=VS.85).aspx">D3DDECLTYPE</a>, <a href="https://msdn.microsoft.com/en-us/library/Bb172558(v=VS.85).aspx">D3DFORMAT</a>, and <a href="https://msdn.microsoft.com/en-us/library/Bb173059(v=VS.85).aspx">DXGI_FORMAT</a> objects.
    </div><div> </div>

## -struct-fields




### -field x

Signed 8-bit integer value in the range [-127, 127] describing the
			    x-coordinate of the vector.
			


### -field y

Signed 8-bit integer value in the range [-127, 127] describing the
			    y-coordinate of the vector.
			


### -field z

Signed 8-bit integer value in the range [-127, 127] describing the
			    z-coordinate of the vector.
			


### -field w

Signed 8-bit integer value in the range [-127, 127] describing the
			    w-coordinate of the vector.
			


### -field v

Unsigned 32-bit integer representing the 4D vector.
		    


### -field XMBYTE4

TBD 


### -field operator=

TBD 




## -remarks



<code>XMBYTE4</code> can be loaded into instances of <a href="https://msdn.microsoft.com/1a044094-444d-e787-fa6a-76e88531aef1">XMVECTOR</a> by using
	    <a href="https://msdn.microsoft.com/e8a3ffb9-72cc-4ef1-a5f8-889d9c19cb48">XMLoadByte4</a>.
	

Instances of <code>XMVECTOR</code> can be stored into an instance of <code>XMBYTE4</code> with <a href="https://msdn.microsoft.com/en-us/library/Ee420224(v=VS.85).aspx">XMStoreByte4</a>.
	

<b>Namespace:</b> Use DirectX::PackedVector

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/58acb05d-e79b-8f42-4cf4-76ae57929739">DirectXMath Library Structures</a>



<a href="https://msdn.microsoft.com/en-us/library/Ee415259(v=VS.85).aspx">XMBYTE4 Extensions</a>
 

 

