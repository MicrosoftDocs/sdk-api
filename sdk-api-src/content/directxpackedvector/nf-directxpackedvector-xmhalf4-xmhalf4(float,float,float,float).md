---
UID: NF:directxpackedvector.XMHALF4.XMHALF4(float,float,float,float)
title: XMHALF4 function
author: windows-sdk-content
description: Initializes a new instance of XMHALF4 from four float arguments.
old-location: dxmath\xmhalf4_ctor_4.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.reference.XMHALF4.#ctor(float,float,float,float)
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: XMHALF4 constructor [DirectX Math Support APIs], XMHALF4 constructor [DirectX Math Support APIs],XMHALF4 structure, XMHALF4 structure [DirectX Math Support APIs],XMHALF4 constructor, XMHALF4.XMHALF4(float,float,float,float), dxmath.xmhalf4_ctor_4
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DirectXPackedVector.h
api_name:
 - XMHALF4.XMHALF4
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- XMHALF4
: 
---

# XMHALF4 function


## -description


Initializes a new instance of <code>XMHALF4</code> from four <code>float</code> arguments.
    

This constructor initializes a new instance of <a href="https://msdn.microsoft.com/194CC053-8341-4E26-B8B2-5F137B201D80">XMHALF4</a> from four
	<code>float</code> arguments.
<div class="alert"><b>Note</b>  This constructor is only available under C++.
    </div><div> </div>

## -parameters




### -param _x

Value of the x-coordinate of the vector, the <b>x</b> member of the new
		    <code>XMHALF4</code> instance.
		


### -param _y

Value of the y-coordinate of the vector, the <b>y</b> member of the new
		    <code>XMHALF4</code> instance.
		


### -param _z

Value of the z-coordinate of the vector, the <b>z</b> member of the new
		    <code>XMHALF4</code> instance.
		


### -param _w

Value of the w-coordinate of the vector, the <b>w</b> member of the new
		    <code>XMHALF4</code> instance.
		


## -remarks



If the magnitude of one of this constructor's floating point arguments cannot be
	    represented by the <code>HALF</code> type, the corresponding member of the new instance of
	    <code>XMHALF4</code> will be infinity for a 16-bit integer (+0x7FFF).
	

The following pseudocode demonstrates the operation of this constructor using the XNA
	    Math <a href="https://msdn.microsoft.com/463abe18-b8c4-44be-9740-b7e0459d3ebd">XMConvertFloatToHalf</a> function:
	

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
	XMHALF4 instance;

	instance.x = XMConvertFloatToHalf(_x);
	instance.y = XMConvertFloatToHalf(_y);
	instance.z = XMConvertFloatToHalf(_z);
	instance.w = XMConvertFloatToHalf(_w);

    </pre>
</td>
</tr>
</table></span></div>



## -see-also




<b>Reference</b>



<a href="https://msdn.microsoft.com/463abe18-b8c4-44be-9740-b7e0459d3ebd">XMConvertFloatToHalf</a>



<a href="https://msdn.microsoft.com/194CC053-8341-4E26-B8B2-5F137B201D80">XMHALF4</a>



<a href="https://msdn.microsoft.com/9a27ff98-5dd1-4db0-b1a1-7c2fa8b53027">XMHALF4 Constructors</a>
 

 

