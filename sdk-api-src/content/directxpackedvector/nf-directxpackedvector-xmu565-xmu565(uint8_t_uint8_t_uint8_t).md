---
UID: NF:directxpackedvector.XMU565.XMU565(uint8_t,uint8_t,uint8_t)
title: XMU565::XMU565(uint8_t,uint8_t,uint8_t) (directxpackedvector.h)
description: Initializes a new instance of XMU565 from three int8_t arguments.
helpviewer_keywords: ["XMU565","XMU565 constructor [DirectX Math Support APIs]","XMU565 constructor [DirectX Math Support APIs]","XMU565 structure","XMU565 structure [DirectX Math Support APIs]","XMU565 constructor","XMU565.XMU565","XMU565.XMU565()","XMU565.XMU565(uint8_t","uint8_t","uint8_t)","XMU565::XMU565","XMU565::XMU565(uint8_t","uint8_t","uint8_t)","dxmath.xmu565_ctor_1"]
old-location: 
tech.root: dxmath
ms.assetid: 184982ed-d1e7-462c-9cac-0393228bf64d
ms.date: 05/06/2019
ms.keywords: XMU565, XMU565 constructor [DirectX Math Support APIs], XMU565 constructor [DirectX Math Support APIs],XMU565 structure, XMU565 structure [DirectX Math Support APIs],XMU565 constructor, XMU565.XMU565, XMU565.XMU565(), XMU565.XMU565(uint8_t,uint8_t,uint8_t), XMU565::XMU565, XMU565::XMU565(uint8_t,uint8_t,uint8_t), dxmath.xmu565_ctor_1
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
 - XMU565::XMU565
 - directxpackedvector/XMU565::XMU565
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
 - XMU565.XMU565
---

# XMU565::XMU565(uint8_t,uint8_t,uint8_t)


## -description

Initializes a new instance of <a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmu565">XMU565</a> from three <code>int8_t</code> arguments.

This constructor initializes a new instance of <wdcml:xref rid="dxmath.xmu565" targtype="struct">XMU565 </wdcml:xref> from three <code>int8_t</code> arguments.

<div class="alert"><b>Note</b>  This is only available for C++ based development.</div>

## -parameters

### -param _x

Value of the x-coordinate of the vector, the **x** member of the new **XMU565** instance.

The magnitude of this argument will be clamped to a range of [0, 31].

### -param _y

Value of the y-coordinate of the vector, the **y** member of the new **XMU565** instance.

The magnitude of this argument will be clamped to a range of [0, 63].

### -param _z

Value of the z-coordinate of the vector, the **z** member of the new **XMU565** instance.

The magnitude of this argument will be clamped to a range of [0, 31].

## -remarks

The following pseudocode demonstrates the operation of this constructor, which takes advantage of the union of the three components of the **XMU565** vector with an instance of **uint16_t** in the definition of the structure:

```cpp
XMU565 instance;
_x1=min( max( _x, 0 ), 31 );
_y1=min( max( _y, 0 ), 63 );
_z1=min( max( _z, 0 ), 31 );

instance.v= ((z & 0x1F) << 11) |
            ((y & 0x3F) << 5) |
            ((x & 0x1F));
```

## -see-also

<a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmu565">XMU565</a>

<a href="/windows/desktop/dxmath/xmu565-ctor">XMU565 Constructors</a>