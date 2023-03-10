---
UID: NF:directxpackedvector.XMU555.XMU555(constuint8_t,bool)
title: XMU555::XMU555(const uint8_t,bool) (directxpackedvector.h)
description: Initializes a new instance of XMU555 from a three element int8_t array and one bool argument.
helpviewer_keywords: ["XMU555","XMU555 constructor [DirectX Math Support APIs]","XMU555 constructor [DirectX Math Support APIs]","XMU555 structure","XMU555 structure [DirectX Math Support APIs]","XMU555 constructor","XMU555.XMU555","XMU555.XMU555()","XMU555.XMU555(const uint8_t","bool)","XMU555::XMU555","XMU555::XMU555(const uint8_t","bool)","dxmath.xmu555_ctor_1"]
old-location: 
tech.root: dxmath
ms.assetid: 6b7e7e6c-93af-4990-9ff9-2b072e88b48b
ms.date: 05/06/2019
ms.keywords: XMU555, XMU555 constructor [DirectX Math Support APIs], XMU555 constructor [DirectX Math Support APIs],XMU555 structure, XMU555 structure [DirectX Math Support APIs],XMU555 constructor, XMU555.XMU555, XMU555.XMU555(), XMU555.XMU555(const uint8_t,bool), XMU555::XMU555, XMU555::XMU555(const uint8_t,bool), dxmath.xmu555_ctor_1
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

# XMU555::XMU555(const uint8_t,bool)


## -description

Initializes a new instance of <a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmu555">XMU555</a> from a three element <code>int8_t</code> array and one <code>bool</code> argument.

This constructor initializes a new instance of **XMU555** from a three element <code>int8_t</code> array (specifying x-, y- and z-components) and one <<code>bool</code> argument (specifying a w-component).

<div class="alert"><b>Note</b>  This is only available for C++ based development.</div>

## -parameters

### -param pArray

Three element character array containing the values used to initialize the x-, y- and z-components of a new instance of **XMU555**.

### -param _w

The value of the instance's w-component.

## -remarks

Array elements and the **_w** argument are mapped to the vector components of a new instance of **XMU555** as follows:

| XMU555 Member | Argument | Range |
|---------------|----------|-------|
| x | pArray[0] | 0, 31 |
| y | pArray[1] | 0, 31 |
| z | pArray[2] | 0, 31 |
| w | _w | 0, 1 |

Arguments to the constructors will be clamped to the permitted range prior to assignment to the appropriate member of **XMU555**.

The following pseudocode demonstrates the operation of this constructor, which takes advantage of the union of the four components of the **XMU555** vector with an instance of **uint16_t** in the definition of the structure:

```cpp
XMU555 instance;
_x1=min( max( pArray[0], 0 ), 31 );
_y1=min( max( pArray[1], 0 ), 31 );
_z1=min( max( pArray[2], 0 ), 31 );
_w1=min( max( _w, 0 ), 1 );

instance.v =  (((uint16_t)_w1 ? 0x8000 : 0) |
              (((uint16_t)_z1 & 0x1F) << 10) |
              (((uint16_t)_y1 & 0x1F) << 5) |  
              (((uint16_t)_x1 & 0x1F)));
```

## -see-also

<a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmu555">XMU555</a>

<a href="/windows/desktop/dxmath/xmu555-ctor">XMU555 Constructors</a>