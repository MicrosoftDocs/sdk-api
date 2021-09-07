---
UID: NF:directxpackedvector.XMXDEC4.XMXDEC4(float,float,float,float)
title: XMXDEC4::XMXDEC4(float,float,float,float) (directxpackedvector.h)
description: Initializes a new instance of XMXDEC4 from four float arguments.
helpviewer_keywords: ["XMXDEC4","XMXDEC4 constructor [DirectX Math Support APIs]","XMXDEC4 constructor [DirectX Math Support APIs]","XMXDEC4 structure","XMXDEC4 structure [DirectX Math Support APIs]","XMXDEC4 constructor","XMXDEC4.XMXDEC4","XMXDEC4.XMXDEC4(float","float","float","float)","XMXDEC4::XMXDEC4","XMXDEC4::XMXDEC4(float","float","float","float)","dxmath.xmxdec4_ctor_3"]
old-location: dxmath\xmxdec4_ctor_3.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.reference.XMXDEC4.#ctor(float,float,float,float)
ms.date: 12/05/2018
ms.keywords: XMXDEC4, XMXDEC4 constructor [DirectX Math Support APIs], XMXDEC4 constructor [DirectX Math Support APIs],XMXDEC4 structure, XMXDEC4 structure [DirectX Math Support APIs],XMXDEC4 constructor, XMXDEC4.XMXDEC4, XMXDEC4.XMXDEC4(float,float,float,float), XMXDEC4::XMXDEC4, XMXDEC4::XMXDEC4(float,float,float,float), dxmath.xmxdec4_ctor_3
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
 - XMXDEC4::XMXDEC4
 - directxpackedvector/XMXDEC4::XMXDEC4
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
 - XMXDEC4.XMXDEC4
---

# XMXDEC4::XMXDEC4(float,float,float,float)


## -description

Initializes a new instance of <code>XMXDEC4</code> from four <code>float</code> arguments.
    

This constructor initializes a new instance of <a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmxdec4">XMXDEC4 </a> from four
	<code>float</code> arguments.
<div class="alert"><b>Note</b>  This constructor is only available under C++.
    </div><div> </div>

## -parameters

### -param _x

Value of the x-coordinate of the vector, the <b>x</b> member of the new
		    <code>XMXDEC4</code> instance.
		

The magnitude of this argument will be clamped to a range of [-511.0,
		    511.0].

### -param _y

Value of the y-coordinate of the vector, the <b>y</b> member of the new
		    <code>XMXDEC4</code> instance.
		

The magnitude of this argument will be clamped to a range of [-511.0,
		    511.0].

### -param _z

Value of the z-coordinate of the vector, the <b>z</b> member of the new
		    <code>XMXDEC4</code> instance.
		

The magnitude of this argument will be clamped to a range of [-511.0,
		    511.0].

### -param _w

Value of the w-coordinate of the vector, the <b>w</b> member of the new
		    <code>XMXDEC4</code> instance.
		

The magnitude of this argument will be clamped to a range of [0.0, 3.0].

## -remarks

The following pseudocode demonstrates the operation of this constructor, which takes
	    advantage of the <code>union</code> of the four components of the <code>XMXDEC4</code> vector with an instance of <code>uint32_t</code> in the definition of the structure:
	


```

	XMXDEC4 instance;
	_x1=min( max( _x, -511.0 ), 511.0 );
	_y1=min( max( _y, -511.0 ), 511.0 );
	_z1=min( max( _z, -511.0 ), 511.0 );
	_w1=min( max( _w, 0.0 ), 3.0 );


	instance.v =  ( (int32_t)_w1 << 30) |
                      (((int32_t)_z1 & 0x3FF) << 20) |
                      (((int32_t)_y1 & 0x3FF) << 10) |
                      (((uint32_t)_x1 & 0x3FF));;
      
```

## -see-also

<b>Reference</b>



<a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmxdec4">XMXDEC4</a>



<a href="/windows/desktop/dxmath/xmxdec4-ctor">XMXDEC4 Constructors</a>