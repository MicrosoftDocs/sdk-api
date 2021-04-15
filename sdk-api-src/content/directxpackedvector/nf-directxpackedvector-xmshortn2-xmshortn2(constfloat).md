---
UID: NF:directxpackedvector.XMSHORTN2.XMSHORTN2(constfloat)
title: XMSHORTN2::XMSHORTN2(const float) (directxpackedvector.h)
description: Initializes a new instance of XMSHORTN2 from a two element float array argument.
helpviewer_keywords: ["XMSHORTN2","XMSHORTN2 constructor [DirectX Math Support APIs]","XMSHORTN2 constructor [DirectX Math Support APIs]","XMSHORTN2 structure","XMSHORTN2 structure [DirectX Math Support APIs]","XMSHORTN2 constructor","XMSHORTN2.XMSHORTN2","XMSHORTN2.XMSHORTN2()","XMSHORTN2.XMSHORTN2(const float)","XMSHORTN2::XMSHORTN2","XMSHORTN2::XMSHORTN2(const float)","dxmath.xmshortn2_ctor_1"]
old-location: 
tech.root: dxmath
ms.assetid: ff110a88-4c5e-4f1a-b04e-c8aa8e00d2b8
ms.date: 05/06/2019
ms.keywords: XMSHORTN2, XMSHORTN2 constructor [DirectX Math Support APIs], XMSHORTN2 constructor [DirectX Math Support APIs],XMSHORTN2 structure, XMSHORTN2 structure [DirectX Math Support APIs],XMSHORTN2 constructor, XMSHORTN2.XMSHORTN2, XMSHORTN2.XMSHORTN2(), XMSHORTN2.XMSHORTN2(const float), XMSHORTN2::XMSHORTN2, XMSHORTN2::XMSHORTN2(const float), dxmath.xmshortn2_ctor_1
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
 - XMSHORTN2::XMSHORTN2
 - directxpackedvector/XMSHORTN2::XMSHORTN2
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
 - XMSHORTN2.XMSHORTN2
---

# XMSHORTN2::XMSHORTN2(const float)


## -description

Initializes a new instance of <a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmshortn2">XMSHORTN2</a> from a two element <code>float</code> array argument.

This constructor initializes a new instance of **XMSHORTN2** from a two element <code>float</code> array argument.

<div class="alert"><b>Note</b>  This constructor is only available under C++.</div>

## -parameters

### -param pArray

Two element floating point array containing the values used to initialize the two components of a new instance of **XMSHORTN2**.

## -remarks

Array elements are mapped to the vector components of a new instance of **XMSHORTN2** as follows:

| Vector Component | Array Element | Range | Description |
|------------------|---------------|-------|--|
| x | pArray[0] | -1.0, 1.0 | During instantiation, pArray[0] is clamped between -1 and 1, multiplied by 32767.0f and assigned to x. |
| y | pArray[1] | -1.0, 1.0 | During instantiation, pArray[1] is clamped between -1 and 1, multiplied by 32767.0f, and then assigned to y. |

The following pseudocode demonstrates the operation of this constructor:

```cpp
XMSHORTN2 instance;
_x1=min( max( pArray[0], -1.0 ), 1.0 );
_y1=min( max( pArray[1], -1.0 ), 1.0 );
_x1 = round( _x1 * 32767.0f);
_y1 = round( _y1 * 32767.0f);
instance._x = _x1;
instance._y = _y1;
```

## -see-also

<a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmshortn2">XMSHORTN2</a>

<a href="/windows/desktop/dxmath/xmshortn2-ctor">XMSHORTN2 Constructors</a>