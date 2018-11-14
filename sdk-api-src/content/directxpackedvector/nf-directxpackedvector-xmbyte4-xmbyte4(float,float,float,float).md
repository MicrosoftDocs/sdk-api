---
UID: NF:directxpackedvector.XMBYTE4.XMBYTE4(float,float,float,float)
title: XMBYTE4 function
author: windows-sdk-content
description: Initializes a new instance of XMBYTE4 from four float arguments.
old-location: dxmath\xmbyte4_ctor_4.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.reference.XMBYTE4.#ctor(float,float,float,float)
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: XMBYTE4 constructor [DirectX Math Support APIs], XMBYTE4 constructor [DirectX Math Support APIs],XMBYTE4 structure, XMBYTE4 structure [DirectX Math Support APIs],XMBYTE4 constructor, XMBYTE4.XMBYTE4(float,float,float,float), dxmath.xmbyte4_ctor_4
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
 - XMBYTE4.XMBYTE4
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- XMBYTE4
: 
---

# XMBYTE4 function


## -description


Initializes a new instance of <code>XMBYTE4</code> from four <code>float</code> arguments.
    

This constructor initializes a new instance of <a href="https://msdn.microsoft.com/087c32f0-f43e-487a-9bdb-6c8739d5a04d">XMBYTE4</a> from four
	<code>float</code> arguments.
<div class="alert"><b>Note</b>  This constructor is only available under C++.</div><div> </div>

## -parameters




### -param _x

Value of the x-coordinate of the vector, the <b>x</b> member of the new 
          <code>XMBYTE4</code> instance.


### -param _y

Value of the y-coordinate of the vector, the <b>y</b> member of the new 
          <code>XMBYTE4</code> instance.


### -param _z

Value of the z-coordinate of the vector, the <b>z</b> member of the new 
          <code>XMBYTE4</code> instance.


### -param _w

Value of the w-coordinate of the vector, the <b>w</b> member of the new 
          <code>XMBYTE4</code> instance.


## -remarks



The magnitude of each argument to the constructor will be clamped to the range supported by an
	   8-bit signed integer [-127.0, 127.0].
       

The following pseudocode demonstrates the operation of this constructor:
      

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
	XMBYTE4 instance;

	instance.x = (int8_t)min( max( _x, -127.0 ), 127.0 );
	instance.y = (int8_t)min( max( _y, -127.0 ), 127.0 );
	instance.z = (int8_t)min( max( _z, -127.0 ), 127.0 );
	instance.w = (int8_t)min( max( _w, -127.0 ), 127.0 );

    </pre>
</td>
</tr>
</table></span></div>



## -see-also




<b>Reference</b>



<a href="https://msdn.microsoft.com/087c32f0-f43e-487a-9bdb-6c8739d5a04d">XMBYTE4</a>



<a href="https://msdn.microsoft.com/c3374ac6-1550-437f-9ffc-fcad46181ed7">XMBYTE4 Constructors</a>
 

 

