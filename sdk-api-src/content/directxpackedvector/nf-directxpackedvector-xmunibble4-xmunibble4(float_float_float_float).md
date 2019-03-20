---
UID: NF:directxpackedvector.XMUNIBBLE4.XMUNIBBLE4(float,float,float,float)
title: XMUNIBBLE4::XMUNIBBLE4(float,float,float,float) (directxpackedvector.h)
author: windows-sdk-content
description: Initializes a new instance of XMUNIBBLE4 from four float arguments.
old-location: dxmath\xmunibble4_ctor_5.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.reference.XMUNIBBLE4.#ctor(float,float,float,float)
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: XMUNIBBLE4, XMUNIBBLE4 constructor [DirectX Math Support APIs], XMUNIBBLE4 constructor [DirectX Math Support APIs],XMUNIBBLE4 structure, XMUNIBBLE4 structure [DirectX Math Support APIs],XMUNIBBLE4 constructor, XMUNIBBLE4.XMUNIBBLE4, XMUNIBBLE4.XMUNIBBLE4(float,float,float,float), XMUNIBBLE4::XMUNIBBLE4, XMUNIBBLE4::XMUNIBBLE4(float,float,float,float), dxmath.xmunibble4_ctor_5
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
 - XMUNIBBLE4.XMUNIBBLE4
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# XMUNIBBLE4::XMUNIBBLE4(float,float,float,float)


## -description


Initializes a new instance of <code>XMUNIBBLE4</code> from four <code>float</code> arguments.
    

This constructor initializes a new instance of <a href="https://msdn.microsoft.com/en-us/library/Ee420614(v=VS.85).aspx">XMUNIBBLE4 </a> from four
	<code>float</code> arguments.
<div class="alert"><b>Note</b>  This constructor is only available under C++.</div><div> </div>

## -parameters




### -param _x

Value of the x-coordinate of the vector, the <b>x</b> member of the new
		    <code>XMUNIBBLE4</code> instance.
		

The magnitude of this argument will be clamped to a range of [0, 15.0].
		


### -param _y

Value of the y-coordinate of the vector, the <b>y</b> member of the new
		    <code>XMUNIBBLE4</code> instance.
		

The magnitude of this argument will be clamped to a range of [0, 15.0].
		


### -param _z

Value of the z-coordinate of the vector, the <b>z</b> member of the new
		    <code>XMUNIBBLE4</code> instance.
		

The magnitude of this argument will be clamped to a range of [0, 15.0].
		


### -param _w

Value of the w-coordinate of the vector, the <b>w</b> member of the new
		    <code>XMUNIBBLE4</code> instance.
		

The magnitude of this argument will be clamped to a range of [0, 15.0].
		


## -remarks



The following pseudocode demonstrates the operation of this constructor, which takes
	    advantage of the <code>union</code> of the four components of the <code>XMUNIBBLE4</code>vector with an instance of <code>uint16_t</code> in the definition of the structure:
	


```

	XMUNIBBLE4 instance;
	_x1=min( max( _x, 0.0 ), 15.0f );
	_y1=min( max( _y, 0.0 ), 15.0f );
	_z1=min( max( _z, 0.0 ), 15.0f );
	_w1=min( max( _w, 0.0 ), 15.0f );

	instance.v =  ( (uint16_t)_w1 << 12) |
                      (((uint16_t)_z1 & 0xF) << 8) |
                      (((uint16_t)_y1 & 0xF) << 4) |
                      (((uint16_t)_x1 & 0xF));
      
```





## -see-also




<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/Ee420614(v=VS.85).aspx">XMUNIBBLE4</a>



<a href="https://msdn.microsoft.com/en-us/library/Ee415488(v=VS.85).aspx">XMUNIBBLE4 Constructors</a>
 

 

