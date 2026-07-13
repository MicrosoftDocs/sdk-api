---
UID: NF:directxpackedvector.XMU555.XMU555(float,float,float,bool)
title: XMU555::XMU555(float,float,float,bool) (directxpackedvector.h)
description: Initializes a new instance of XMU555 from three float and one bool arguments.
helpviewer_keywords: ["XMU555","XMU555 constructor [DirectX Math Support APIs]","XMU555 constructor [DirectX Math Support APIs]","XMU555 structure","XMU555 structure [DirectX Math Support APIs]","XMU555 constructor","XMU555.XMU555","XMU555.XMU555(float","float","float","bool)","XMU555::XMU555","XMU555::XMU555(float","float","float","bool)","dxmath.xmu555_ctor_5"]
old-location: dxmath\xmu555_ctor_5.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.reference.XMU555.#ctor(float,float,float,bool)
ms.date: 12/05/2018
ms.keywords: XMU555, XMU555 constructor [DirectX Math Support APIs], XMU555 constructor [DirectX Math Support APIs],XMU555 structure, XMU555 structure [DirectX Math Support APIs],XMU555 constructor, XMU555.XMU555, XMU555.XMU555(float,float,float,bool), XMU555::XMU555, XMU555::XMU555(float,float,float,bool), dxmath.xmu555_ctor_5
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
 - XMU555::XMU555
 - directxpackedvector/XMU555::XMU555
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
 - XMU555.XMU555
---

# XMU555::XMU555(float,float,float,bool)


## -description

Initializes a new instance of <code>XMU555</code> from three <code>float</code> and one
	<code>bool</code> arguments.
    

This constructor initializes a new instance of <a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmu555">XMU555 </a> from three
	<code>float</code> (specifying x-, y-, and z-components) and one <code>bool</code> (specifying
	the w-component) arguments.
<div class="alert"><b>Note</b>  This constructor is only available under C++.
    </div><div> </div>

## -parameters

### -param _x

Value of the x-coordinate of the vector, the <b>x</b> member of the new
		    <code>XMU555</code> instance.
		

The magnitude of this argument will be clamped to a range of [0, 31.0].

### -param _y

Value of the y-coordinate of the vector, the <b>y</b> member of the new
		    <code>XMU555</code> instance.
		

The magnitude of this argument will be clamped to a range of [0, 31.0].

### -param _z

Value of the z-coordinate of the vector, the <b>z</b> member of the new
		    <code>XMU555</code> instance.
		

The magnitude of this argument will be clamped to a range of [0, 31.0].

### -param _w

Value of the w-coordinate of the vector, the <b>w</b> member of the new
		    <code>XMU555</code> instance.
		

The magnitude of this argument will be clamped to a range of [0, 1].

## -remarks

The following pseudocode demonstrates the operation of this constructor, which takes
	    advantage of the <code>union</code> of the four components of the <code>XMU555</code> vector with an instance of <code>uint16_t</code> in the definition of the structure:
	


```

	_x1=min( max( _x, 0.0 ), 31.0 );
	_y1=min( max( _y, 0.0 ), 31.0 );
	_z1=min( max( _z, 0.0 ), 31.0 );
	_w1=min( max( _w, 0 ), 1 );

	instance.v =  (((uint16_t)_w1 ? 0x8000 : 0) |
                      (((uint16_t)_z1 & 0x1F) << 10) |
                      (((uint16_t)_y1 & 0x1F) << 5) |  
		      (((uint16_t)_x1 & 0x1F)));
	
```

## -see-also

<b>Reference</b>



<a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmu555">XMU555</a>



<a href="/windows/desktop/dxmath/xmu555-ctor">XMU555 Constructors</a>