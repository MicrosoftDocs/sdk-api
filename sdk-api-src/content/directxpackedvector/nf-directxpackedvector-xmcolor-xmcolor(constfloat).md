---
UID: NF:directxpackedvector.XMCOLOR.XMCOLOR(constfloat)
title: XMCOLOR::XMCOLOR(const float) (directxpackedvector.h)
description: Initializes a new instance of XMCOLOR from a four element float array argument.
helpviewer_keywords: ["XMCOLOR","XMCOLOR constructor [DirectX Math Support APIs]","XMCOLOR constructor [DirectX Math Support APIs]","XMCOLOR structure","XMCOLOR structure [DirectX Math Support APIs]","XMCOLOR constructor","XMCOLOR.XMCOLOR","XMCOLOR.XMCOLOR()","XMCOLOR.XMCOLOR(const float)","XMCOLOR::XMCOLOR","XMCOLOR::XMCOLOR(const float)","dxmath.xmcolor_ctor_1"]
old-location: 
tech.root: dxmath
ms.assetid: 1cd1f6e7-c596-47b4-8d28-f537060659bc
ms.date: 05/06/2019
ms.keywords: XMCOLOR, XMCOLOR constructor [DirectX Math Support APIs], XMCOLOR constructor [DirectX Math Support APIs],XMCOLOR structure, XMCOLOR structure [DirectX Math Support APIs],XMCOLOR constructor, XMCOLOR.XMCOLOR, XMCOLOR.XMCOLOR(), XMCOLOR.XMCOLOR(const float), XMCOLOR::XMCOLOR, XMCOLOR::XMCOLOR(const float), dxmath.xmcolor_ctor_1
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
 - XMCOLOR::XMCOLOR
 - directxpackedvector/XMCOLOR::XMCOLOR
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
 - XMCOLOR.XMCOLOR
---

# XMCOLOR::XMCOLOR(const float)


## -description

Initializes a new instance of <a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmcolor">XMCOLOR</a> from a four element <code>float</code> array argument.

This constructor initializes a new instance of **XMCOLOR** from a from a four element <code>float</code> array argument.

<div class="alert"><b>Note</b>  This is only available for C++ based development.</div>

## -parameters

### -param pArray

Four element floating point array containing the color values used to initialize the four components of a new instance of **XMCOLOR**.

## -remarks

Array elements are mapped to the vector components of a new instance of **XMCOLOR** as follows:

| Vector Component | Array Element | Range | Description |
|------------------|---------------|-------|--|
| a | pArray[0] | 0.0, 1.0 | During instantiation, pArray[0] is clamped between 0 and 1, multiplied by 255.0f and assigned to a (alpha channel). |
| r | pArray[1] | 0.0, 1.0 | During instantiation, pArray[1] is clamped between 0 and 1, multiplied by 255.0f, and then assigned to r (red channel). |
| z | pArray[2] | 0.0, 1.0 | During instantiation, pArray[2] is clamped between 0 and 1, multiplied by 255.0f, and then assigned to g (green channel). |
| w | pArray[3] | 0.0, 1.0 | During instantiation, pArray[3] is clamped between 0 and 1, multiplied by 255.0f, and then assigned to b (blue channel). |

The following pseudocode demonstrates the operation of this constructor, which takes advantage of the *union* of the four color channels of the **XMCOLOR** structure with an instance of <code>uint32_t</code> in the definition of the structure:

```cpp
XMCOLOR instance;
_a1 = min( max( pArray[0], 0.0 ), 1.0 );
_r1 = min( max( pArray[1], 0.0 ), 1.0 );
_g1 = min( max( pArray[2], 0.0 ), 1.0 );
_b1 = min( max( pArray[3], 0.0 ), 1.0 );

_a1 = round ( _a1 * 255.0f );
_r1 = round ( _r1 * 255.0f );
_g1 = round ( _g1 * 255.0f );
_b1 = round ( _b1 * 255.0f );

instance.v =  ( (uint32_t)_a1 << 24) |
              ( (uint32_t)_r1 << 16) |
              ( (uint32_t)_b1 <<  8) |
              ( (uint32_t)_b1 );
```

## -see-also

<a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmcolor">XMCOLOR</a>

<a href="/windows/desktop/dxmath/xmcolor-ctor">XMCOLOR Constructors</a>