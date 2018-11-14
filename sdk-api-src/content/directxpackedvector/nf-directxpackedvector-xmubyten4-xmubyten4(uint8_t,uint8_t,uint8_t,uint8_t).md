---
UID: NF:directxpackedvector.XMUBYTEN4.XMUBYTEN4(uint8_t,uint8_t,uint8_t,uint8_t)
title: XMUBYTEN4 function
author: windows-sdk-content
description: Initializes a new instance of XMUBYTEN4 from four uint8_t arguments.
old-location: dxmath\xmubyten4_ctor_3.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.reference.XMUBYTEN4.#ctor(uint8_t,uint8_t,uint8_t,uint8_t)
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: XMUBYTEN4 constructor [DirectX Math Support APIs], XMUBYTEN4 constructor [DirectX Math Support APIs],XMUBYTEN4 structure, XMUBYTEN4 structure [DirectX Math Support APIs],XMUBYTEN4 constructor, XMUBYTEN4.XMUBYTEN4(uint8_t,uint8_t,uint8_t,uint8_t), dxmath.xmubyten4_ctor_3
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
 - XMUBYTEN4.XMUBYTEN4
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- XMUBYTEN4
: 
---

# XMUBYTEN4 function


## -description


Initializes a new instance of <code>XMUBYTEN4</code> from four <code>uint8_t</code> arguments.
    

This constructor initializes a new instance of <a href="https://msdn.microsoft.com/552002c1-0000-44a6-9f43-9c958a8d1aa3">XMUBYTEN4 
	</a> from a
	four <code>uint8_t</code> arguments.
<div class="alert"><b>Note</b>  This constructor is only available under C++.</div><div> </div>

## -parameters




### -param _x

Value of the x-coordinate of the vector, the <b>x</b> member of the new
		    <code>XMUBYTEN4</code> instance.
		


### -param _y

Value of the y-coordinate of the vector, the <b>y</b> member of the new
		    <code>XMUBYTEN4</code> instance.
		


### -param _z

Value of the z-coordinate of the vector, the <b>z</b> member of the new
		    <code>XMUBYTEN4</code> instance.
		


### -param _w

Value of the w-coordinate of the vector, the <b>w</b> member of the new
		    <code>XMUBYTEN4</code> instance.
		


## -remarks



Input values are not normalized. The following pseudocode demonstrates the operation of
	    this constructor:
	

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
	    XMUBYTEN4 instance;

	    instance.x = _x; 
	    instance.y = _y; 
	    instance.z = _z; 
	    instance.w = _w;

	</pre>
</td>
</tr>
</table></span></div>



## -see-also




<b>Reference</b>



<a href="https://msdn.microsoft.com/552002c1-0000-44a6-9f43-9c958a8d1aa3">XMUBYTEN4</a>



<a href="https://msdn.microsoft.com/0bb46e9b-6c76-40b5-9bf0-6387edfed484">XMUBYTEN4 Constructors</a>
 

 

