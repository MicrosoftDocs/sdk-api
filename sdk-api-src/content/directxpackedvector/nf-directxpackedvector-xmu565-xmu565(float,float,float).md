---
UID: NF:directxpackedvector.XMU565.XMU565(float,float,float)
title: XMU565 function
author: windows-sdk-content
description: Initializes a new instance of XMU565 from three float arguments.
old-location: dxmath\xmu565_ctor_5.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.reference.XMU565.#ctor(float,float,float)
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: XMU565 constructor [DirectX Math Support APIs], XMU565 constructor [DirectX Math Support APIs],XMU565 structure, XMU565 structure [DirectX Math Support APIs],XMU565 constructor, XMU565.XMU565(float,float,float), dxmath.xmu565_ctor_5
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
 - XMU565.XMU565
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- XMU565
: 
---

# XMU565 function


## -description


Initializes a new instance of <code>XMU565</code> from three <code>float</code> arguments.
    

This constructor initializes a new instance of <a href="https://msdn.microsoft.com/58c9ee71-d038-4664-9fac-5a074b60e9c3">XMU565 </a> from three
	<code>float</code> arguments.
<div class="alert"><b>Note</b>  This constructor is only available under C++.</div><div> </div>

## -parameters




### -param _x

Value of the x-coordinate of the vector, the <b>x</b> member of the new
		    <code>XMU565</code> instance.
		

The magnitude of this argument will be clamped to a range of [0.0, 31.0].
		


### -param _y

Value of the y-coordinate of the vector, the <b>y</b> member of the new
		    <code>XMU565</code> instance.
		

The magnitude of this argument will be clamped to a range of [0.0, 63.0].
		


### -param _z

Value of the z-coordinate of the vector, the <b>z</b> member of the new
		    <code>XMU565</code> instance.
		

The magnitude of this argument will be clamped to a range of [0.0, 31.0].
		


## -remarks



The following pseudocode demonstrates the operation of this constructor, which takes
	    advantage of the <code>union</code> of the three components of the <code>XMU565</code> vector
	    with an instance of <code>uint16_t</code> in the definition of the structure:
	

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
	XMU565 instance;
	_x1=min( max( _x, 0.0 ), 31.0 );
	_y1=min( max( _y, 0.0 ), 63.0 );
	_z1=min( max( _z, 0.0 ), 31.0 );

	instance.v= ((z &amp; 0x1F) &lt;&lt; 11) |
                    ((y &amp; 0x3F) &lt;&lt; 5) |
                    ((x &amp; 0x1F));
      </pre>
</td>
</tr>
</table></span></div>



## -see-also




<b>Reference</b>



<a href="https://msdn.microsoft.com/58c9ee71-d038-4664-9fac-5a074b60e9c3">XMU565</a>



<a href="https://msdn.microsoft.com/d482dbf5-081c-4a1b-a81f-63d21d46a489">XMU565 Constructors</a>
 

 

