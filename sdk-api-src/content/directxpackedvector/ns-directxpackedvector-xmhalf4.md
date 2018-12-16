---
UID: NS:directxpackedvector.XMHALF4
title: XMHALF4
author: windows-sdk-content
description: Describes a 4D vector consisting of four half-precision (16-bit) floating-point values.
old-location: dxmath\xmhalf4.htm
tech.root: dxmath
ms.assetid: T:Microsoft.directx_sdk.reference.XMHALF4
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: XMHALF4, XMHALF4 structure [DirectX Math Support APIs], directxpackedvector/XMHALF4, dxmath.xmhalf4
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
 - XMHALF4
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# XMHALF4 structure


## -description


Describes a 4D vector consisting of four half-precision (16-bit) floating-point values.
    



For a list of additional functionality such as constructors and operators that are available
	using <code>XMHALF4</code> when you are programming in C++, see <a href="https://msdn.microsoft.com/en-us/library/Ee415322(v=VS.85).aspx">XMHALF4 Extensions</a>.
<div class="alert"><b>Note</b>  See <a href="https://msdn.microsoft.com/31512657-c413-9e6e-e343-1ea677a02b8c">DirectXMath Library Type
	Equivalences</a> for information about equivalent <a href="https://msdn.microsoft.com/en-us/library/Bb172533(v=VS.85).aspx">D3DDECLTYPE</a>, <a href="https://msdn.microsoft.com/en-us/library/Bb172558(v=VS.85).aspx">D3DFORMAT</a>, and <a href="https://msdn.microsoft.com/en-us/library/Bb173059(v=VS.85).aspx">DXGI_FORMAT</a> objects.
    </div><div> </div>

## -struct-fields




### -field x

<b>HALF</b> value describing the x-coordinate.
		


### -field y

<b>HALF</b> value describing the y-coordinate.
		


### -field z

<b>HALF</b> value describing the z-coordinate.
		


### -field w

<b>HALF</b> value describing the w-coordinate.
		


### -field v

 


### -field XMHALF4

TBD 


### -field operator=

TBD 




## -remarks



The definition of the <code>HALF</code> type used under DirectXMath is consistent with the <a href="http://ieeexplore.ieee.org/xpl/freeabs_all.jsp?arnumber=4610935">IEEE
	    standard</a>, and consists of a sign bit, a 5 bit biased exponent, and a 10 bit
	    mantissa:
	

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
                    [15] SEEEEEMMMMMMMMMM [0]
	</pre>
</td>
</tr>
</table></span></div>
<code>XMHALF4</code> can be loaded into instances of <a href="https://msdn.microsoft.com/1a044094-444d-e787-fa6a-76e88531aef1"> XMVECTOR</a> by
	    using <a href="https://msdn.microsoft.com/a17c391c-1c40-4c3e-b915-7b2690a17eb5">XMLoadHalf4</a>.
	

Instances of <code>XMVECTOR</code> can be stored into an instance of <code>XMHALF4</code> with <a href="https://msdn.microsoft.com/en-us/library/Ee420355(v=VS.85).aspx">XMStoreHalf4</a>.
	

<b>Namespace:</b> Use DirectX::PackedVector

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/58acb05d-e79b-8f42-4cf4-76ae57929739">DirectXMath Library Structures</a>



<a href="https://msdn.microsoft.com/en-us/library/Ee415322(v=VS.85).aspx">XMHALF4 Extensions</a>
 

 

