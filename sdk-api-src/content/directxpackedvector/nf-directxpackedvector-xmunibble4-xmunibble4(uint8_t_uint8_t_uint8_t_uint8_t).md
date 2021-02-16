---
UID: NF:directxpackedvector.XMUNIBBLE4.XMUNIBBLE4(uint8_t,uint8_t,uint8_t,uint8_t)
title: XMUNIBBLE4::XMUNIBBLE4(uint8_t,uint8_t,uint8_t,uint8_t) (directxpackedvector.h)
description: Initializes a new instance of XMUNIBBLE4 from four int8_t arguments.
helpviewer_keywords: ["XMUNIBBLE4","XMUNIBBLE4 constructor [DirectX Math Support APIs]","XMUNIBBLE4 constructor [DirectX Math Support APIs]","XMUNIBBLE4 structure","XMUNIBBLE4 structure [DirectX Math Support APIs]","XMUNIBBLE4 constructor","XMUNIBBLE4.XMUNIBBLE4","XMUNIBBLE4.XMUNIBBLE4()","XMUNIBBLE4.XMUNIBBLE4(uint8_t","uint8_t","uint8_t","uint8_t)","XMUNIBBLE4::XMUNIBBLE4","XMUNIBBLE4::XMUNIBBLE4(uint8_t","uint8_t","uint8_t","uint8_t)","dxmath.xmunibble4_ctor_1"]
old-location: 
tech.root: dxmath
ms.assetid: 8e88294c-5e00-48f4-9d08-802dafb85b0e
ms.date: 05/06/2019
ms.keywords: XMUNIBBLE4, XMUNIBBLE4 constructor [DirectX Math Support APIs], XMUNIBBLE4 constructor [DirectX Math Support APIs],XMUNIBBLE4 structure, XMUNIBBLE4 structure [DirectX Math Support APIs],XMUNIBBLE4 constructor, XMUNIBBLE4.XMUNIBBLE4, XMUNIBBLE4.XMUNIBBLE4(), XMUNIBBLE4.XMUNIBBLE4(uint8_t,uint8_t,uint8_t,uint8_t), XMUNIBBLE4::XMUNIBBLE4, XMUNIBBLE4::XMUNIBBLE4(uint8_t,uint8_t,uint8_t,uint8_t), dxmath.xmunibble4_ctor_1
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
 - XMUNIBBLE4::XMUNIBBLE4
 - directxpackedvector/XMUNIBBLE4::XMUNIBBLE4
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
 - XMUNIBBLE4.XMUNIBBLE4
---

# XMUNIBBLE4::XMUNIBBLE4(uint8_t,uint8_t,uint8_t,uint8_t)


## -description

Initializes a new instance of <a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmunibble4">XMUNIBBLE4</a> from four <code>int8_t</code> arguments.

This constructor initializes a new instance of **XMUNIBBLE4** from four <code>int8_t</code> arguments.

<div class="alert"><b>Note</b>  This is only available for C++ based development.</div>

## -parameters

### -param _x

Value of the x-coordinate of the vector, the x member of the new **XMUNIBBLE4** instance.

The magnitude of this argument will be clamped to a range of [0, 15].

### -param _y

Value of the y-coordinate of the vector, the y member of the new **XMUNIBBLE4** instance.

The magnitude of this argument will be clamped to a range of [0, 15].

### -param _z

Value of the z-coordinate of the vector, the z member of the new **XMUNIBBLE4** instance.

The magnitude of this argument will be clamped to a range of [0, 15].

### -param _w

Value of the w-coordinate of the vector, the w member of the new **XMUNIBBLE4** instance.

The magnitude of this argument will be clamped to a range of [0, 15].

## -remarks

The following pseudocode demonstrates the operation of this constructor, which takes advantage of the union of the four components of the **XMUNIBBLE4** vector with an instance of **uint16_t** in the definition of the structure:
	
```cpp
XMUNIBBLE4 instance;
_x1=min( max( _x, 0 ), 15 );
_y1=min( max( _y, 0 ), 15 );
_z1=min( max( _z, 0 ), 15 );
_w1=min( max( _w, 0 ), 15 );

instance.v =  ( (uint16_t)_w1 << 12) |
                (((uint16_t)_z1 & 0xF) << 8) |
                (((uint16_t)_y1 & 0xF) << 4) |
                (((uint16_t)_x1 & 0xF));
```

## -see-also

<a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmunibble4">XMUNIBBLE4</a>

<a href="/windows/desktop/dxmath/xmunibble4-ctor">XMUNIBBLE4 Constructors</a>