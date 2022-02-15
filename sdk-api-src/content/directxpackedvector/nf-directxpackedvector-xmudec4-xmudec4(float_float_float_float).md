---
UID: NF:directxpackedvector.XMUDEC4.XMUDEC4(float,float,float,float)
title: XMUDEC4::XMUDEC4(float,float,float,float) (directxpackedvector.h)
description: Initializes a new instance of XMUDEC4 from four float arguments.
helpviewer_keywords: ["XMUDEC4","XMUDEC4 constructor [DirectX Math Support APIs]","XMUDEC4 constructor [DirectX Math Support APIs]","XMUDEC4 structure","XMUDEC4 structure [DirectX Math Support APIs]","XMUDEC4 constructor","XMUDEC4.XMUDEC4","XMUDEC4.XMUDEC4(float","float","float","float)","XMUDEC4::XMUDEC4","XMUDEC4::XMUDEC4(float","float","float","float)","dxmath.xmudec4_ctor_3"]
old-location: dxmath\xmudec4_ctor_3.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.reference.XMUDEC4.#ctor(float,float,float,float)
ms.date: 12/05/2018
ms.keywords: XMUDEC4, XMUDEC4 constructor [DirectX Math Support APIs], XMUDEC4 constructor [DirectX Math Support APIs],XMUDEC4 structure, XMUDEC4 structure [DirectX Math Support APIs],XMUDEC4 constructor, XMUDEC4.XMUDEC4, XMUDEC4.XMUDEC4(float,float,float,float), XMUDEC4::XMUDEC4, XMUDEC4::XMUDEC4(float,float,float,float), dxmath.xmudec4_ctor_3
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
 - XMUDEC4::XMUDEC4
 - directxpackedvector/XMUDEC4::XMUDEC4
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
 - XMUDEC4.XMUDEC4
---

# XMUDEC4::XMUDEC4(float,float,float,float)


## -description

Initializes a new instance of <code>XMUDEC4</code> from four <code>float</code> arguments.
    

This constructor initializes a new instance of <a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmudec4">XMUDEC4 </a> from four
	<code>float</code> arguments.
<div class="alert"><b>Note</b>  This constructor is only available under C++.
    </div><div> </div>

## -parameters

### -param _x

Value of the x-coordinate of the vector, the <b>x</b> member of the new
		    <code>XMUDEC4</code> instance.
		

The magnitude of this argument will be clamped to a range of [0.0, 1023.0].

### -param _y

Value of the y-coordinate of the vector, the <b>y</b> member of the new
		    <code>XMUDEC4</code> instance.
		

The magnitude of this argument will be clamped to a range of [0.0, 1023.0].

### -param _z

Value of the z-coordinate of the vector, the <b>z</b> member of the new
		    <code>XMUDEC4</code> instance.
		

The magnitude of this argument will be clamped to a range of [0.0, 1023.0].

### -param _w

Value of the w-coordinate of the vector, the <b>w</b> member of the new
		    <code>XMUDEC4</code> instance.
		

The magnitude of this argument will be clamped to a range of [0.0, 3.0].

## -remarks

The following pseudocode demonstrates the operation of this constructor, which takes
	    advantage of the <code>union</code> of the four components of the <code>XMUDEC4</code> vector with an instance of <code>uint32_t</code> in the definition of the structure:
	


```

	XMUDEC4 instance;
	_x1=min( max( _x, 0.0.0 ), 1023.0 );
	_y1=min( max( _y, 0.0.0 ), 1023.0 );
	_z1=min( max( _z, 0.0.0 ), 1023.0 );
	_w1=min( max( _w, 0.0 ), 3.0 );


	instance.v =  ( (uint32_t)_w1 << 30) |
                      (((uint32_t)_z1 & 0x3FF) << 20) |
                      (((uint32_t)_y1 & 0x3FF) << 10) |
                      (((uint32_t)_x1 & 0x3FF));;
      
```

## -see-also

<b>Reference</b>



<a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmudec4">XMUDEC4</a>



<a href="/windows/desktop/dxmath/xmudec4-ctor">XMUDEC4 Constructors</a>