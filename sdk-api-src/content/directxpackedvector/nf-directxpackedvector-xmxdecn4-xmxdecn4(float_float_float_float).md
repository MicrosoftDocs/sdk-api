---
UID: NF:directxpackedvector.XMXDECN4.XMXDECN4(float,float,float,float)
title: XMXDECN4::XMXDECN4(float,float,float,float) (directxpackedvector.h)
description: Initializes a new instance of XMXDECN4 from four normalized floatarguments.
helpviewer_keywords: ["XMXDECN4","XMXDECN4 constructor [DirectX Math Support APIs]","XMXDECN4 constructor [DirectX Math Support APIs]","XMXDECN4 structure","XMXDECN4 structure [DirectX Math Support APIs]","XMXDECN4 constructor","XMXDECN4.XMXDECN4","XMXDECN4.XMXDECN4(float","float","float","float)","XMXDECN4::XMXDECN4","XMXDECN4::XMXDECN4(float","float","float","float)","dxmath.xmxdecn4_ctor_3"]
old-location: dxmath\xmxdecn4_ctor_3.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.reference.XMXDECN4.#ctor(float,float,float,float)
ms.date: 12/05/2018
ms.keywords: XMXDECN4, XMXDECN4 constructor [DirectX Math Support APIs], XMXDECN4 constructor [DirectX Math Support APIs],XMXDECN4 structure, XMXDECN4 structure [DirectX Math Support APIs],XMXDECN4 constructor, XMXDECN4.XMXDECN4, XMXDECN4.XMXDECN4(float,float,float,float), XMXDECN4::XMXDECN4, XMXDECN4::XMXDECN4(float,float,float,float), dxmath.xmxdecn4_ctor_3
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
 - XMXDECN4::XMXDECN4
 - directxpackedvector/XMXDECN4::XMXDECN4
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
 - XMXDECN4.XMXDECN4
---

# XMXDECN4::XMXDECN4(float,float,float,float)


## -description

Initializes a new instance of <code>XMXDECN4</code> from four normalized <code>float</code> arguments.
    

This constructor initializes a new instance of <a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmxdecn4">XMXDECN4</a> from four
	normalized <code>float</code> arguments.
<div class="alert"><b>Note</b>  This constructor is only available under C++.
    </div><div> </div>

## -parameters

### -param _x

A normalized value for the x-coordinate of the vector.
		

This argument should be between -1.0 and 1.0; during the instantiation of an
		    instance of <code>XMXDECN4</code>, it is multiplied by <code>511.0f</code> and then
		    stored as the <b>x</b> member of the structure.

### -param _y

A normalized value for the y-coordinate of the vector, the <b>y</b> of the
		    new instance of <code>XMXDECN4</code>.
		

This argument should be between -1.0 and 1.0; during the instantiation of an
		    instance of <code>XMXDECN4</code>, it is multiplied by <code>511.0f</code> and then
		    stored as the <b>y</b> member of the structure.

### -param _z

A normalized value for the z-coordinate of the vector, the <b>z</b> of the
		    new instance of <code>XMXDECN4</code>.
		

This argument should be between -1.0 and 1.0; during the instantiation of an
		    instance of <code>XMXDECN4</code>, it is multiplied by <code>511.0f</code> and then
		    stored as the <b>z</b> member of the structure.

### -param _w

A normalized value for the w-coordinate of the vector, the <b>w</b> of the
		    new instance of <code>XMXDECN4</code>.
		

This argument should be between -1.0 and 1.0; during the instantiation of
		    an instance of <a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmcolor">XMCOLOR</a>, it is multiplied by <code>3.0f</code> and then
		    stored as the <b>w</b> member of the structure.

## -remarks

All input values,<i>_x</i>,<i>_y</i>, <i>_z</i>, and <i>_w</i> are
	    clamped to a range of -1.0 to 1.0.
	

The following pseudocode demonstrates the operation of this constructor, which takes
	    advantage of the <code>union</code> of the four components of the <code>XMDECN4</code> vector with an instance of <code>uint32_t</code> in the definition of the structure:
	


```

    	XMDECN4 instance;
	_x1=min( max( _x, -1.0 ), 1.0 );
	_y1=min( max( _y, -1.0 ), 1.0 );
	_z1=min( max( _z, -1.0 ), 1.0 );
	_w1=min( max( _w, 0.0 ), 1.0 );
	_x1 = round( _x1 *  511.0f);
	_y1 = round( _y1 *  511.0f);
	_z1 = round( _z1 *  511.0f);
	_w1 = round( _w1 *  3.0f);

	instance.v =  ( (int32_t)_w1 << 30) |
                      (((int32_t)_z1 & 0x3FF) << 20) |
                      (((int32_t)_y1 & 0x3FF) << 10) |
                      (((uint32_t)_x1 & 0x3FF));
	
```

## -see-also

<b>Reference</b>



<a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmxdecn4">XMXDECN4</a>



<a href="/windows/desktop/dxmath/xmxdecn4-ctor">XMXDECN4 Constructors</a>