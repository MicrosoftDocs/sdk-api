---
UID: NF:directxpackedvector.XMUBYTEN2.XMUBYTEN2(float,float)
title: XMUBYTEN2::XMUBYTEN2(float,float)
author: windows-sdk-content
description: Initializes a new instance of XMUBYTEN2 from two float arguments.
old-location: dxmath\xmubyten2_ctor_4.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.reference.XMUBYTEN2.#ctor(float,float)
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: XMUBYTEN2, XMUBYTEN2 constructor [DirectX Math Support APIs], XMUBYTEN2 constructor [DirectX Math Support APIs],XMUBYTEN2 structure, XMUBYTEN2 structure [DirectX Math Support APIs],XMUBYTEN2 constructor, XMUBYTEN2.XMUBYTEN2, XMUBYTEN2.XMUBYTEN2(float,float), XMUBYTEN2::XMUBYTEN2, XMUBYTEN2::XMUBYTEN2(float,float), dxmath.xmubyten2_ctor_4
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - XMUBYTEN2.XMUBYTEN2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# XMUBYTEN2::XMUBYTEN2(float,float)


## -description


Initializes a new instance of <code>XMUBYTEN2</code> from two <code>float</code> arguments.

This constructor initializes a new instance of <a href="https://msdn.microsoft.com/e6faa9a7-fedc-45cb-8480-df179ad3bd86">XMUBYTEN2 </a> from two <code>float</code> arguments.
<div class="alert"><b>Note</b>  This constructor is only available with C++.</div><div> </div>

## -parameters




### -param _x

A normalized value for the x-coordinate of the vector.

This argument should be between 0.0 and 1.0. During the instantiation of an instance 
        of <code>XMUBYTEN2</code>, it is
        multiplied by <code>255.0f</code>, and then stored as the <b>x</b> member of the structure.


### -param _y

A normalized value for the y-coordinate of the vector, the <b>y</b> 
        of the new instance of <code>XMUBYTEN2</code>.

This argument should be between 0.0 and 1.0. During the instantiation of an instance 
        of <code>XMUBYTEN2</code>, it is
        multiplied by <code>255.0f</code>, and then stored as the <b>y</b> member of the structure.


## -remarks



The magnitude of each argument to the constructor will be clamped to the range supported by an 8-bit unsigned integer
   [0, 255.0].

The following pseudocode demonstrates the operation of this constructor, which takes advantage of the <code>union</code>of the four components of the <code>XMUBYTEN2</code> vector with an instance of <code>uint32_t</code> in the definition of
   the structure:

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
	XMUBYTEN2 instance;
	_x1=min( max( _x, 0.0 ), 1.0 );
	_y1=min( max( _y, 0.0 ), 1.0 );
	_x = round( _x *  255.0f);
	_y = round( _y *  255.0f);
	instance.x = (uint8_t)_x1;
	instance.y = (uint8_t)_y1;
    </pre>
</td>
</tr>
</table></span></div>



## -see-also




<b>Reference</b>



<a href="https://msdn.microsoft.com/e6faa9a7-fedc-45cb-8480-df179ad3bd86">XMUBYTEN2</a>



<a href="https://msdn.microsoft.com/aa72906c-1338-49cf-909c-4d3a00aa3de2">XMUBYTEN2 Constructors</a>
 

 

