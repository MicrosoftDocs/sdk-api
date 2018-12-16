---
UID: NS:directxpackedvector.XMUDECN4
title: XMUDECN4
author: windows-sdk-content
description: A 4D vector for storing unsigned, normalized integer values as 10 bit unsigned x-, y-, and z-components and a 2-bit unsigned w-component.
old-location: dxmath\xmudecn4.htm
tech.root: dxmath
ms.assetid: T:Microsoft.directx_sdk.reference.XMUDECN4
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: XMUDECN4, XMUDECN4 structure [DirectX Math Support APIs], directxpackedvector/XMUDECN4, dxmath.xmudecn4
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
 - XMUDECN4
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# XMUDECN4 structure


## -description


A 4D vector for storing unsigned, normalized integer values as 10 bit unsigned x-, y-, 
  and z-components and a 2-bit unsigned w-component.
    

For a list of more functionality such as constructors and operators that are available
	using <code>XMUDECN4</code> when you are programming in C++, see <a href="https://msdn.microsoft.com/en-us/library/Ee415454(v=VS.85).aspx">XMUDECN4 Extensions</a>.
<div class="alert"><b>Note</b>  See <a href="https://msdn.microsoft.com/31512657-c413-9e6e-e343-1ea677a02b8c">DirectXMath Library Type
	Equivalences</a> for information about equivalent <a href="https://msdn.microsoft.com/en-us/library/Bb172533(v=VS.85).aspx">D3DDECLTYPE</a>, <a href="https://msdn.microsoft.com/en-us/library/Bb172558(v=VS.85).aspx">D3DFORMAT</a>, and <a href="https://msdn.microsoft.com/en-us/library/Bb173059(v=VS.85).aspx">DXGI_FORMAT</a> objects.
    </div><div> </div>

## -struct-fields




### -field x

Unsigned integer value in the range [0, 1023] describing the
			    x-coordinate of the vector.
			


### -field y

Unsigned integer value in the range [0, 1023] describing the
			    y-coordinate of the vector.
			


### -field z

Unsigned integer value in the range [0, 1023] describing the
			    z-coordinate of the vector.
			


### -field w

Unsigned integer value in the range [0, 3] describing the w-coordinate
			    of the vector.
			


### -field v

Unsigned 32-bit integer representing the 4D vector.
		    


### -field XMUDECN4

TBD 


### -field operator uint32_t

TBD 


### -field operator=

TBD 




## -remarks



Those <code>XMUDECN4</code> constructors using floating point arguments require normalized input,
	    which must be in the range of [0.-1.0].  During instantiation, the inputs specifying the x-, y-,
	    and z-components are multiplied by 1023.0f, and the w-component are multiplied by 3.0f.
      The results are rounded, and then assigned to the appropriate members of <code>XMUDECN4</code>.
	

You can use <code>XMUDECN4</code> to load instances of <a href="https://msdn.microsoft.com/1a044094-444d-e787-fa6a-76e88531aef1">XMVECTOR</a> from normalized values 
      by using <a href="https://msdn.microsoft.com/0ac3215a-08c3-4a7e-96ea-b9421e7cfe03">XMLoadUDecN4</a>, which divides the x-, y-, and
	    z-components by 1023.0f, divides the w-component by 3.0f, rounds the result, and then assigns
	    the components to an <code>XMVECTOR</code> instance.
	

<code>XMVECTOR</code> instances containing normalized values can be stored into <code>XMUDECN4</code>using <a href="https://msdn.microsoft.com/en-us/library/Ee420379(v=VS.85).aspx">XMStoreUDecN4</a>, which multiplies the x-, y-, and z-components by
	    1023.0f, multiplies the w-component by 3.0f, and rounds the result before assigning the values 
      to the appropriate <code>XMUDECN4</code> members.
	

<b>Namespace:</b> Use DirectX::PackedVector

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/58acb05d-e79b-8f42-4cf4-76ae57929739">DirectXMath Library Structures</a>



<a href="https://msdn.microsoft.com/en-us/library/Ee415454(v=VS.85).aspx">XMUDECN4 Extensions</a>
 

 

