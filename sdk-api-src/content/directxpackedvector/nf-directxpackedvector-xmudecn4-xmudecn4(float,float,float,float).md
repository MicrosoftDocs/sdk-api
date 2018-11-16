---
UID: NF:directxpackedvector.XMUDECN4.XMUDECN4(float,float,float,float)
title: XMUDECN4 function
author: windows-sdk-content
description: This constructor initializes a new instance of XMUDECN4 from four normalized float arguments.
old-location: dxmath\xmudecn4_ctor_3.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.reference.XMUDECN4.#ctor(float,float,float,float)
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: XMUDECN4 constructor [DirectX Math Support APIs], XMUDECN4 constructor [DirectX Math Support APIs],XMUDECN4 structure, XMUDECN4 structure [DirectX Math Support APIs],XMUDECN4 constructor, XMUDECN4.XMUDECN4(float,float,float,float), dxmath.xmudecn4_ctor_3
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
 - XMUDECN4.XMUDECN4
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- XMUDECN4
: 
---

# XMUDECN4 function


## -description



This constructor initializes a new instance of <a href="https://msdn.microsoft.com/4b85445e-8ea9-4e1c-b07e-db13d2ee82aa">XMUDECN4</a> from four
	normalized <code>float</code> arguments.


<div class="alert"><b>Note</b>  This constructor is only available under C++.
    </div><div> </div>

## -parameters




### -param _x

A normalized value for the x-coordinate of the vector.
		

This argument should be between 0.0 and 1.0; during the instantiation of an
		    instance of <code>XMUDECN4</code>, it is multiplied by <code>1023.0f</code> and then
		    stored as the <b>x</b> member of the structure.
		


### -param _y

A normalized value for the y-coordinate of the vector, the <b>y</b> of the
		    new instance of <code>XMUDECN4</code>.
		

This argument should be between 0.0 and 1.0; during the instantiation of an
		    instance of <code>XMUDECN4</code>, it is multiplied by <code>1023.0f</code> and then
		    stored as the <b>y</b> member of the structure.
		


### -param _z

A normalized value for the z-coordinate of the vector, the <b>z</b> of the
		    new instance of <code>XMUDECN4</code>.
		

This argument should be between 0.0 and 1.0; during the instantiation of an
		    instance of <code>XMUDECN4</code>, it is multiplied by <code>1023.0f</code> and then
		    stored as the <b>z</b> member of the structure.
		


### -param _w

A normalized value for the w-coordinate of the vector, the <b>w</b> of the
		    new instance of <code>XMUDECN4</code>.
		

This argument should be between -1.0 and 1.0; during the instantiation of
		    an instance of <a href="https://msdn.microsoft.com/B799AA06-C51B-440A-93AD-3D3334449E27">XMCOLOR</a>, it is multiplied by <code>3.0f</code> and then
		    stored as the <b>w</b> member of the structure.
		


## -remarks



All input values,<i>_x</i>,<i>_y</i>, <i>_z</i>, and <i>_w</i> are
	    clamped to a range of -1.0 to 1.0.
	

The following pseudocode demonstrates the operation of this constructor, which takes
	    advantage of the <code>union</code> of the four components of the <code>XMDECN4</code>vector with an instance of <code>uint32_t</code> in the definition of the structure:
	

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
    	XMDECN4 instance;
	_x1=min( max( _x, 0.0 ), 1.0 );
	_y1=min( max( _y, 0.0 ), 1.0 );
	_z1=min( max( _z, 0.0 ), 1.0 );
	_w1=min( max( _w, 0.0 ), 1.0 );
	_x = round( _x *  1023.0f);
	_y = round( _y *  1023.0f);
	_z = round( _z *  1023.0f);
	_w = round( _w *  3.0f);

	instance.v =  ( (uint32_t)_w1 &lt;&lt; 30) |
                      (((uint32_t)_z1 &amp; 0x3FF) &lt;&lt; 20) |
                      (((uint32_t)_y1 &amp; 0x3FF) &lt;&lt; 10) |
                      (((uint32_t)_x1 &amp; 0x3FF));
	</pre>
</td>
</tr>
</table></span></div>



## -see-also




<b>Reference</b>



<a href="https://msdn.microsoft.com/4b85445e-8ea9-4e1c-b07e-db13d2ee82aa">XMUDECN4</a>



<a href="https://msdn.microsoft.com/6e513f04-08fc-4f77-a19d-66d719abdb23">XMUDECN4 Constructors</a>
 

 

