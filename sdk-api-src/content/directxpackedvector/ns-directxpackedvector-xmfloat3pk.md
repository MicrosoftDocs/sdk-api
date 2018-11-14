---
UID: NS:directxpackedvector.XMFLOAT3PK
title: XMFLOAT3PK
author: windows-sdk-content
description: Describes a 3D vector with X and Y components stored as 11 bit floating point number, and Z component stored as a 10 bit floating-point value.
old-location: dxmath\xmfloat3pk.htm
tech.root: dxmath
ms.assetid: T:Microsoft.directx_sdk.reference.XMFLOAT3PK
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: XMFLOAT3PK, XMFLOAT3PK structure [DirectX Math Support APIs], directxpackedvector/XMFLOAT3PK, dxmath.xmfloat3pk
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
 - XMFLOAT3PK
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# XMFLOAT3PK structure


## -description


Describes a 3D vector with X and Y components stored as 11 bit floating point number, and Z
	component stored as a 10 bit floating-point value.
    

For a list of additional functionality, such as constructors and operators, available using
	<code>XMFLOAT3PK</code> when programming in C++, see <a href="https://msdn.microsoft.com/cca32fd6-9f41-49c2-8e2a-247bbf78edca">XMFLOAT3PK Extensions</a>.


## -struct-fields




### -field xm

 


### -field xe

 


### -field ym

 


### -field ye

 


### -field zm

 


### -field ze

 


### -field v

Unsigned 32-bit integer representing the 3D vector.
		    


#### - xe : 5

The 5-bit biased exponent for the x component.
			


#### - xm : 6

The 6-bit mantissa for the x component.
			


#### - ye : 5

The 5-bit biased exponent for the y component.
			


#### - ym : 6

The 6-bit mantissa for the y component.
			


#### - ze : 5

The 5-bit biased exponent for the z component.
			


#### - zm : 5

The 5-bit mantissa for the z component.
			


## -remarks



There are no sign bits. This means all partial-precision numbers are positive. The z
	    component is stored in the most significant bits, and the x component is stored in the
	    least significant bits like this:
	

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
  (Z10Y11X11): [31] ZZZZZzzz zzYYYYYy yyyyyXXX XXxxxxxx [0]
</pre>
</td>
</tr>
</table></span></div>
Or in detail:
     

<ul>
<li>
Bits 0-5 of <b>v</b> are the 6 bit <i>mantissa</i> of the <b>x</b>component's floating point value: the <b>xm</b> member of the structure.
	     

</li>
<li>
Bits 6-10 of <b>v</b> are the 5 bit <i>exponent</i> of the
		 <b>x</b> component's floating point value the <b>xe</b> member of the structure.
	     

</li>
<li>
Bits 11-16 of <b>v</b> are the 6-bit <i>mantissa</i> of the
		 <b>y</b> component's floating point value: the <b>ym</b> member of the
		 structure.
	     

</li>
<li>
Bits 17-21 of <b>v</b> are the 5 bit <i>exponent</i> of the
		 <b>y</b> component's floating point value: the <b>ye</b> member of the
		 structure.
	     

</li>
<li>
Bits 22-26 of <b>v</b> are the 5 bit <i>mantissa</i> of the
		 <b>z</b> component's floating point value: the <b>zm</b> member of the
		 structure.
	     

</li>
<li>
Bits 27-31 of <b>v</b> are the 5 bit <i>exponent</i> of the
		 <b>z</b> component's floating point value: the <b>ze</b> member of the
		 structure.
	     

</li>
</ul>
<code>XMFLOAT3PK</code> can be loaded into instances of <a href="https://msdn.microsoft.com/1a044094-444d-e787-fa6a-76e88531aef1"> XMVECTOR</a> by using <a href="https://msdn.microsoft.com/2d96b209-0374-465b-bb81-1df17996550d">XMLoadFloat3PK</a>.


Instances of <code>XMVECTOR</code> can be stored into an instance of <code>XMFLOAT3PK</code> with <a href="https://msdn.microsoft.com/b358dce3-2444-47c7-9b26-44a9abf8cdb5">XMStoreFloat3PK</a>.


MIN_F10 / MIN_F11 = 6.10352e-5

MAX_F10 = 64512

MAX_F11 = 65024

<b>Namespace:</b> Use DirectX::PackedVector

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/58acb05d-e79b-8f42-4cf4-76ae57929739">DirectXMath Library Structures</a>



<a href="https://msdn.microsoft.com/cca32fd6-9f41-49c2-8e2a-247bbf78edca">XMFLOAT3PK Extensions</a>
 

 

