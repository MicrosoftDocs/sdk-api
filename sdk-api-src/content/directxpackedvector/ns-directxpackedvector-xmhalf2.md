---
UID: NS:directxpackedvector.XMHALF2
title: XMHALF2
author: windows-sdk-content
description: A 2D vector consisting of two half-precision (16bit) floating-point values.
old-location: dxmath\xmhalf2.htm
tech.root: dxmath
ms.assetid: T:Microsoft.directx_sdk.reference.XMHALF2
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: XMHALF2, XMHALF2 structure [DirectX Math Support APIs], directxpackedvector/XMHALF2, dxmath.xmhalf2
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
 - XMHALF2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# XMHALF2 structure


## -description


A 2D vector consisting of two half-precision (16bit) floating-point values.
    



For a list of additional functionality such as constructors and operators that are available
	using <code>XMHALF2</code> when you are programming in C++, see <a href="https://msdn.microsoft.com/3e2995bf-e755-4665-bf97-6b9190e78ab5">XMHALF2 Extensions</a>.
<div class="alert"><b>Note</b>  See <a href="https://msdn.microsoft.com/31512657-c413-9e6e-e343-1ea677a02b8c">DirectXMath Library Type
	Equivalences</a> for information about equivalent <a href="https://msdn.microsoft.com/993fc7e4-4752-4bce-82d0-0a034fdc69c0">D3DDECLTYPE</a>, <a href="https://msdn.microsoft.com/a222e3bb-310c-4019-93ee-6a2da2a46ded">D3DFORMAT</a>, and <a href="https://msdn.microsoft.com/dce61bc4-4ed5-4e64-84e8-6db88025e5c2">DXGI_FORMAT</a> objects.
    </div><div> </div>

## -struct-fields




### -field x

<b>HALF</b> value describing the x-coordinate.
		


### -field y

<b>HALF</b> value describing the y-coordinate.
		


### -field v

 




## -remarks



The definition of the <code>HALF</code> type used under DirectXMath is consistent with the <a href="http://ieeexplore.ieee.org/xpl/freeabs_all.jsp?arnumber=4610935">IEEE
	    standard</a>, and consists of a sign bit, a 5 bit biased exponent, and a 10 bit
	    mantissa:
	


```

                    [15] SEEEEEMMMMMMMMMM [0]
	
```


<code>XMHALF2</code>can be loaded into instances of <a href="https://msdn.microsoft.com/1a044094-444d-e787-fa6a-76e88531aef1">XMVECTOR</a> by using <a href="https://msdn.microsoft.com/d12a9d56-07dd-4a1b-a0b7-46026e82e63d">XMLoadHalf2</a>.
	

Instances of <code>XMVECTOR</code> can be stored into an instance of <code>XMHALF2</code> with <a href="https://msdn.microsoft.com/7c1a1c31-aeed-4938-ab0a-536f782b53fc">XMStoreHalf2</a>.
	

<b>Namespace:</b> Use DirectX::PackedVector

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/58acb05d-e79b-8f42-4cf4-76ae57929739">DirectXMath Library Structures</a>



<a href="https://msdn.microsoft.com/3e2995bf-e755-4665-bf97-6b9190e78ab5">XMHALF2 Extensions</a>
 

 

