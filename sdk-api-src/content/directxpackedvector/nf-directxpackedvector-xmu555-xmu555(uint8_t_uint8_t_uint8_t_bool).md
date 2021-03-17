---
UID: NF:directxpackedvector.XMU555.XMU555(uint8_t,uint8_t,uint8_t,bool)
title: XMU555::XMU555(uint8_t,uint8_t,uint8_t,bool) (directxpackedvector.h)
description: Initializes a new instance of XMU555 from three int8_t and one bool arguments.
helpviewer_keywords: ["XMU555","XMU555 constructor [DirectX Math Support APIs]","XMU555 constructor [DirectX Math Support APIs]","XMU555 structure","XMU555 structure [DirectX Math Support APIs]","XMU555 constructor","XMU555.XMU555","XMU555.XMU555()","XMU555.XMU555(uint8_t","uint8_t","uint8_t","bool)","XMU555::XMU555","XMU555::XMU555(uint8_t","uint8_t","uint8_t","bool)","dxmath.xmu555_ctor_1"]
old-location: 
tech.root: dxmath
ms.assetid: 0895544c-7381-419d-9928-3ac3baa80920
ms.date: 05/06/2019
ms.keywords: XMU555, XMU555 constructor [DirectX Math Support APIs], XMU555 constructor [DirectX Math Support APIs],XMU555 structure, XMU555 structure [DirectX Math Support APIs],XMU555 constructor, XMU555.XMU555, XMU555.XMU555(), XMU555.XMU555(uint8_t,uint8_t,uint8_t,bool), XMU555::XMU555, XMU555::XMU555(uint8_t,uint8_t,uint8_t,bool), dxmath.xmu555_ctor_1
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

# XMU555::XMU555(uint8_t,uint8_t,uint8_t,bool)


## -description

Initializes a new instance of <a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmu555">XMU555</a> from three <code>int8_t</code> and one <code>bool</code> arguments.

This constructor initializes a new instance of **XMU555** from three <code>int8_t</code> (specifying x-, y-, and z-components) and one <code>bool</code> (specifying a w-component) arguments.

<div class="alert"><b>Note</b>  This is only available for C++ based development.</div>

## -parameters

### -param _x

Value of the x-coordinate of the vector, the **x** member of the new **XMU555** instance.

The magnitude of this argument will be clamped to a range of [0, 31].

### -param _y

Value of the y-coordinate of the vector, the **y** member of the new **XMU555** instance.

The magnitude of this argument will be clamped to a range of [0, 31].

### -param _z

Value of the z-coordinate of the vector, the **z** member of the new **XMU555** instance.

The magnitude of this argument will be clamped to a range of [0, 31].

### -param _w

Value of the w-coordinate of the vector, the <wdcml:mark type="member">w</wdcml:mark> member of the new **XMU555** instance.

The magnitude of this argument will be clamped to a range of [0, 1].

## -remarks

The following pseudocode demonstrates the operation of this constructor, which takes advantage of the union of the four components of the **XMU555** vector with an instance of **uint16_t** in the definition of the structure:

```cpp
XMU555 instance;
_x1=min( max( _x, 0 ), 31 );
_y1=min( max( _y, 0 ), 31 );
_z1=min( max( _z, 0 ), 31 );
_w1=min( max( _w, 0 ), 1 );

instance.v =  (((uint16_t)_w1) ? 0x8000 : 0) |
              (((uint16_t)_z1 & 0x1F) << 10) |
              (((uint16_t)_y1 & 0x1F) << 5) |
              (((uint16_t)_x1 & 0x1F));
```

## -see-also

<a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmu555">XMU555</a>

<a href="/windows/desktop/dxmath/xmu555-ctor">XMU555 Constructors</a>