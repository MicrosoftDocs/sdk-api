---
UID: NF:directxpackedvector.XMBYTEN4.XMBYTEN4(float,float,float,float)
title: XMBYTEN4::XMBYTEN4(float,float,float,float) (directxpackedvector.h)
description: Initializes a new instance of XMBYTEN4 from four float arguments.
helpviewer_keywords: ["XMBYTEN4","XMBYTEN4 constructor [DirectX Math Support APIs]","XMBYTEN4 constructor [DirectX Math Support APIs]","XMBYTEN4 structure","XMBYTEN4 structure [DirectX Math Support APIs]","XMBYTEN4 constructor","XMBYTEN4.XMBYTEN4","XMBYTEN4.XMBYTEN4(float","float","float","float)","XMBYTEN4::XMBYTEN4","XMBYTEN4::XMBYTEN4(float","float","float","float)","dxmath.xmbyten4_ctor_4"]
old-location: dxmath\xmbyten4_ctor_4.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.reference.XMBYTEN4.#ctor(float,float,float,float)
ms.date: 12/05/2018
ms.keywords: XMBYTEN4, XMBYTEN4 constructor [DirectX Math Support APIs], XMBYTEN4 constructor [DirectX Math Support APIs],XMBYTEN4 structure, XMBYTEN4 structure [DirectX Math Support APIs],XMBYTEN4 constructor, XMBYTEN4.XMBYTEN4, XMBYTEN4.XMBYTEN4(float,float,float,float), XMBYTEN4::XMBYTEN4, XMBYTEN4::XMBYTEN4(float,float,float,float), dxmath.xmbyten4_ctor_4
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - XMBYTEN4::XMBYTEN4
 - directxpackedvector/XMBYTEN4::XMBYTEN4
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DirectXPackedVector.h
api_name:
 - XMBYTEN4.XMBYTEN4
---

# XMBYTEN4::XMBYTEN4(float,float,float,float)


## -description

Initializes a new instance of <code>XMBYTEN4</code> from four <code>float</code> arguments.
    

This constructor initializes a new instance of <a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmbyten4">XMBYTEN4 </a> from four
	<code>float</code> arguments.
<div class="alert"><b>Note</b>  This constructor is only available under C++.
    </div><div> </div>

## -parameters

### -param _x

A normalized value for the x-coordinate of the vector.
		

This argument should be between -1.0 and 1.0. During the instantiation of
		    an instance of <code>XMBYTEN4</code>, it is multiplied by <code>127.0f</code> and
		    then stored as the <b>x</b> member of the structure.

### -param _y

A normalized value for the y-coordinate of the vector, the <b>y</b> of the
		    new instance of <code>XMBYTEN4</code>

This argument should be between -1.0 and 1.0. During the instantiation of
      an instance of <code>XMBYTEN4</code>, it is multiplied by <code>127.0f</code> and
		    then stored as the <b>y</b> member of the structure.

### -param _z

A normalized value for the z-coordinate of the vector, the <b>z</b> of the
		    new instance of <code>XMBYTEN4</code>

This argument should be between -1.0 and 1.0. During the instantiation of
      an instance of <code>XMBYTEN4</code>, it is multiplied by <code>127.0f</code> and
		    then stored as the <b>z</b> member of the structure.

### -param _w

A normalized value for the w-coordinate of the vector, the <b>w</b> of the
		    new instance of <code>XMBYTEN4</code>

This argument should be between -1.0 and 1.0. During the instantiation of
      an instance of <code>XMBYTEN4</code>, it is multiplied by <code>127.0f</code> and
		    then stored as the <b>w</b> member of the structure.

## -remarks

The magnitude of each argument to the constructor will be clamped to the range supported
	    by an 8-bit signed integer [-127.0, 127.0].
	

The following pseudocode demonstrates the operation of this constructor, which takes
	    advantage of the <code>union</code> of the four components of the <code>XMBYTEN4</code> vector with an instance of <code>uint32_t</code> in the definition of the structure:
	


```

	XMBYTEN4 instance;
	_x1=min( max( _x, -1.0 ), 1.0 );
	_y1=min( max( _y, -1.0 ), 1.0 );
	_z1=min( max( _z, -1.0 ), 1.0 );
	_w1=min( max( _w, -1.0 ), 1.0 );
	_x1 = round( _x1 *  127.0f);
	_y1 = round( _y1 *  127.0f);
	_z1 = round( _z1 *  127.0f);
	_w1 = round( _w1 *  127.0f);
	instance.x = (int8_t)_x1;
	instance.y = (int8_t)_y1;
	instance.z = (int8_t)_z1;
	instance.w = (int8_t)_w1;
      
```

## -see-also

<b>Reference</b>



<a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmbyten4">XMBYTEN4</a>



<a href="/windows/desktop/dxmath/xmbyten4-ctor">XMBYTEN4 Constructors</a>