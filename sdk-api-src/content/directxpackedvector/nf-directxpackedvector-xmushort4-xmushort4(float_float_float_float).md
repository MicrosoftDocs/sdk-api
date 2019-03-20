---
UID: NF:directxpackedvector.XMUSHORT4.XMUSHORT4(float,float,float,float)
title: XMUSHORT4::XMUSHORT4(float,float,float,float) (directxpackedvector.h)
author: windows-sdk-content
description: Initializes a new instance of XMUSHORT4 from four float arguments.
old-location: dxmath\xmushort4_ctor_4.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.reference.XMUSHORT4.#ctor(float,float,float,float)
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: XMUSHORT4, XMUSHORT4 constructor [DirectX Math Support APIs], XMUSHORT4 constructor [DirectX Math Support APIs],XMUSHORT4 structure, XMUSHORT4 structure [DirectX Math Support APIs],XMUSHORT4 constructor, XMUSHORT4.XMUSHORT4, XMUSHORT4.XMUSHORT4(float,float,float,float), XMUSHORT4::XMUSHORT4, XMUSHORT4::XMUSHORT4(float,float,float,float), dxmath.xmushort4_ctor_4
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
 - XMUSHORT4.XMUSHORT4
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# XMUSHORT4::XMUSHORT4(float,float,float,float)


## -description


Initializes a new instance of <code>XMUSHORT4</code> from four <code>float</code> arguments.
    

This constructor initializes a new instance of <a href="https://msdn.microsoft.com/en-us/library/Ee420702(v=VS.85).aspx">XMUSHORT4</a> from four
	<code>float</code> arguments.
<div class="alert"><b>Note</b>  This constructor is only available under C++.
    </div><div> </div>

## -parameters




### -param _x

Value of the x-coordinate of the vector, the <b>x</b> member of the new
		    <code>XMUSHORT4</code> instance.
		


### -param _y

Value of the y-coordinate of the vector, the <b>y</b> member of the new
		    <code>XMUSHORT4</code> instance.
		


### -param _z

Value of the z-coordinate of the vector, the <b>z</b> member of the new
		    <code>XMUSHORT4</code> instance.
		


### -param _w

Value of the w-coordinate of the vector, the <b>w</b> member of the new
		    <code>XMUSHORT4</code> instance.
		


## -remarks



The magnitude of each argument to the constructor will be clamped to the range supported
	    by an 16-bit unsigned integer [0.0, 65535.0].
	

The following pseudocode demonstrates the operation of this constructor:
	


```

	XMUSHORT4 instance;

	instance.x = (uint16_t)min( max( _x, 0.0 ), 65535.0 );
	instance.y = (uint16_t)min( max( _y, 0.0 ), 65535.0 );
	instance.z = (uint16_t)min( max( _z, 0.0 ), 65535.0 );
	instance.w = (uint16_t)min( max( _w, 0.0 ), 65535.0 );

    
```





## -see-also




<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/Ee420702(v=VS.85).aspx">XMUSHORT4</a>



<a href="https://msdn.microsoft.com/en-us/library/Ee415500(v=VS.85).aspx">XMUSHORT4 Constructors</a>
 

 

