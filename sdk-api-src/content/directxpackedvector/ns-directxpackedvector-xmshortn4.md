---
UID: NS:directxpackedvector.XMSHORTN4
title: XMSHORTN4
author: windows-sdk-content
description: A 4D vector for storing signed, normalized values as signed 16-bit integers, (type int16_t).
old-location: dxmath\xmshortn4.htm
tech.root: dxmath
ms.assetid: T:Microsoft.directx_sdk.reference.XMSHORTN4
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: XMSHORTN4, XMSHORTN4 structure [DirectX Math Support APIs], directxpackedvector/XMSHORTN4, dxmath.xmshortn4
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
 - XMSHORTN4
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# XMSHORTN4 structure


## -description


A 4D vector for storing signed, normalized values as  signed 16-bit integers, (type <code>int16_t</code>).
    



For a list of additional functionality such as constructors and operators that are available
	using <code>XMSHORTN4</code> when you are programming in C++, see <a href="https://msdn.microsoft.com/en-us/library/Ee415435(v=VS.85).aspx">XMSHORTN4 Extensions</a>.
<div class="alert"><b>Note</b>  See <a href="https://msdn.microsoft.com/31512657-c413-9e6e-e343-1ea677a02b8c">DirectXMath Library Type
	Equivalences</a> for information about equivalent <a href="https://msdn.microsoft.com/en-us/library/Bb172533(v=VS.85).aspx">D3DDECLTYPE</a>, <a href="https://msdn.microsoft.com/en-us/library/Bb172558(v=VS.85).aspx">D3DFORMAT</a>, and <a href="https://msdn.microsoft.com/en-us/library/Bb173059(v=VS.85).aspx">DXGI_FORMAT</a> objects.
    </div><div> </div>

## -struct-fields




### -field x

Signed 16-bit integer in the range [-32767, 32767] describing the x-coordinate
		    of the vector.
		


### -field y

Signed 16-bit integer in the range [-32767, 32767] describing the y-coordinate
		    of the vector.
		


### -field z

Signed 16-bit integer in the range [-32767, 32767] describing the z-coordinate
		    of the vector.
		


### -field w

Signed 16-bit integer in the range [-32767, 32767] describing the w-coordinate
		    of the vector.
		


### -field v

 




## -remarks



Those <code>XMSHORTN4</code> constructors using floating point arguments require normalized input,
	    which must be in the range of [-1.0.-1.0].  During instantiation, these data are
	    multiplied by 32767.0f, results are rounded, and then
	    assigned to the appropriate members of <code>XMSHORTN4</code>.

	

<code>XMSHORTN4</code> can be used to load instances of <a href="https://msdn.microsoft.com/1a044094-444d-e787-fa6a-76e88531aef1">XMVECTOR</a> from
	    normalized values, by using <a href="https://msdn.microsoft.com/74cf23de-199a-48e6-81f1-b43762f103b4">XMLoadShortN4</a>, which divides each
	    component 32767.0f, rounds the result, and then assigns the components to an
	    <code>XMVECTOR</code> instance.
	

<code>XMVECTOR</code> instances containing normalized values can be stored into <code>XMSHORTN4</code>using <a href="https://msdn.microsoft.com/en-us/library/Ee420373(v=VS.85).aspx">XMStoreShortN4</a>, which multiplies each component by 32767.0f,
	    rounding the result, before assigning the values to the appropriate <code>XMSHORTN4</code> members.
	

<b>Namespace:</b> Use DirectX::PackedVector

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/58acb05d-e79b-8f42-4cf4-76ae57929739">DirectXMath Library Structures</a>



<a href="https://msdn.microsoft.com/en-us/library/Ee415435(v=VS.85).aspx">XMSHORTN4 Extensions</a>
 

 

