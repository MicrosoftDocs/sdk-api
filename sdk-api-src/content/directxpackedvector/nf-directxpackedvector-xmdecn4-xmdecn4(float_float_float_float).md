---
UID: NF:directxpackedvector.XMDECN4.XMDECN4(float,float,float,float)
title: XMDECN4::XMDECN4(float,float,float,float) (directxpackedvector.h)
description: Initializes a new instance of XMDECN4 from four normalized floatarguments.
helpviewer_keywords: ["XMDECN4","XMDECN4 constructor [DirectX Math Support APIs]","XMDECN4 constructor [DirectX Math Support APIs]","XMDECN4 structure","XMDECN4 structure [DirectX Math Support APIs]","XMDECN4 constructor","XMDECN4.XMDECN4","XMDECN4.XMDECN4(float","float","float","float)","XMDECN4::XMDECN4","XMDECN4::XMDECN4(float","float","float","float)","dxmath.xmdecn4_ctor_3"]
old-location: dxmath\xmdecn4_ctor_3.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.reference.XMDECN4.#ctor(float,float,float,float)
ms.date: 12/05/2018
ms.keywords: XMDECN4, XMDECN4 constructor [DirectX Math Support APIs], XMDECN4 constructor [DirectX Math Support APIs],XMDECN4 structure, XMDECN4 structure [DirectX Math Support APIs],XMDECN4 constructor, XMDECN4.XMDECN4, XMDECN4.XMDECN4(float,float,float,float), XMDECN4::XMDECN4, XMDECN4::XMDECN4(float,float,float,float), dxmath.xmdecn4_ctor_3
f1_keywords:
- directxpackedvector/XMDECN4.XMDECN4
dev_langs:
- c++
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
- XMDECN4.XMDECN4
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# XMDECN4::XMDECN4(float,float,float,float)


## -description


Initializes a new instance of <code>XMDECN4</code> from four normalized <code>float</code>arguments.
    

This constructor initializes a new instance of <a href="https://docs.microsoft.com/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmdecn4">XMDECN4</a> from four
	normalized <code>float</code> arguments.
<div class="alert"><b>Note</b>  This constructor is only available under C++.
    </div><div> </div>

## -parameters




### -param _x

A normalized value for the x-coordinate of the vector.
		

This argument should be between -1.0 and 1.0; during the instantiation of
		    an instance of <code>XMDECN4</code>, it is multiplied by <code>511.0f</code> and
		    then stored as the <b>x</b> member of the structure.
		


### -param _y

A normalized value for the y-coordinate of the vector, the <b>y</b> of the
		    new instance of <code>XMDECN4</code>.
		

This argument should be between -1.0 and 1.0; during the instantiation of
		    an instance of <code>XMDECN4</code>, it is multiplied by <code>511.0f</code> and
		    then stored as the <b>y</b> member of the structure.
		


### -param _z

A normalized value for the z-coordinate of the vector, the <b>z</b> of the
		    new instance of <code>XMDECN4</code>.
		

This argument should be between -1.0 and 1.0; during the instantiation of
		    an instance of <code>XMDECN4</code>, it is multiplied by <code>511.0f</code> and
		    then stored as the <b>z</b> member of the structure.
		


### -param _w

A normalized value for the w-coordinate of the vector, the <b>w</b> of the
		    new instance of <code>XMDECN4</code>.
		

This argument should be between -1.0 and 1.0.
		


## -remarks



All input values,<i>_x</i>,<i>_y</i>, <i>_z</i>, and <i>_w</i> are
	    clamped to a range of -1.0 to 1.0.
	

The following pseudocode demonstrates the operation of this constructor, which takes
	    advantage of the <code>union</code> of the four components of the <code>XMDECN4</code>vector with an instance of <code>uint32_t</code> in the definition of the structure:
	


```

    	XMDECN4 instance;
	_x1=min( max( _x, -1.0 ), 1.0 );
	_y1=min( max( _y, -1.0 ), 1.0 );
	_z1=min( max( _z, -1.0 ), 1.0 );
	_w1=min( max( _w, -1.0 ), 1.0 );
	_x1 = round( _x1 *  511.0f);
	_y1 = round( _y1 *  511.0f);
	_z1 = round( _z1 *  511.0f);


	instance.v =  ( (int32_t)_w1 << 30) |
                      (((int32_t)_z1 & 0x3FF) << 20) |
                      (((int32_t)_y1 & 0x3FF) << 10) |
                      (((int32_t)_x1 & 0x3FF));
	
```





## -see-also




<b>Reference</b>



<a href="https://docs.microsoft.com/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmdecn4">XMDECN4</a>



<a href="https://docs.microsoft.com/windows/desktop/dxmath/xmdecn4-ctor">XMDECN4 Constructors</a>
 

 

