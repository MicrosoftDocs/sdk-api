---
UID: NF:directxpackedvector.XMUDEC4.XMUDEC4(constfloat)
title: XMUDEC4::XMUDEC4(const float) (directxpackedvector.h)
description: Initializes a new instance of XMUDEC4 from a four element float array argument.
helpviewer_keywords: ["XMUDEC4","XMUDEC4 constructor [DirectX Math Support APIs]","XMUDEC4 constructor [DirectX Math Support APIs]","XMUDEC4 structure","XMUDEC4 structure [DirectX Math Support APIs]","XMUDEC4 constructor","XMUDEC4.XMUDEC4","XMUDEC4.XMUDEC4()","XMUDEC4.XMUDEC4(const float)","XMUDEC4::XMUDEC4","XMUDEC4::XMUDEC4(const float)","dxmath.xmudec4_ctor_1"]
old-location: 
tech.root: dxmath
ms.assetid: cf87b946-988a-4088-baa0-a6e7425074ce
ms.date: 05/06/2019
ms.keywords: XMUDEC4, XMUDEC4 constructor [DirectX Math Support APIs], XMUDEC4 constructor [DirectX Math Support APIs],XMUDEC4 structure, XMUDEC4 structure [DirectX Math Support APIs],XMUDEC4 constructor, XMUDEC4.XMUDEC4, XMUDEC4.XMUDEC4(), XMUDEC4.XMUDEC4(const float), XMUDEC4::XMUDEC4, XMUDEC4::XMUDEC4(const float), dxmath.xmudec4_ctor_1
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

# XMUDEC4::XMUDEC4(const float)


## -description

Initializes a new instance of <a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmudec4">XMUDEC4</a> from a four element <code>float</code> array argument.

This constructor initializes a new instance of **XMUDEC4** from a four element <code>float</code> array argument.

<div class="alert"><b>Note</b>  This constructor is only available under C++.</div>

## -parameters

### -param pArray

Four element floating point array containing the values used to initialize the four components of a new instance of **XMUDEC4**.

## -remarks

As **XMUDEC4** represents a four component integer vector, the fractional part of an element of *pArray* will be truncated.

Array elements are mapped to the vector components of a new instance of **XMUDEC4** as follows:

| XMUDEC4 Member | Array Element | Range |
|------------------|---------------|-------|
| x | pArray[0] | -0.0, 1023.0 |
| y | pArray[1] | -0.0, 1023.0 |
| z | pArray[2] | -0.0, 1023.0 |
| w | pArray[3] | 0, 3 |

Elements of *pArray* will be clamped to the permitted range prior to assignment to the appropriate member of **XMUDEC4**.

The following pseudocode demonstrates the operation of this constructor, which takes advantage of the union of the four components of the **XMUDEC4** vector with an instance of **uint32_t** in the definition of the structure:

```cpp
XMUDEC4 instance;
_x1=min( max( pArray[0], 0.0 ), 1023.0 );
_y1=min( max( pArray[1], 0.0 ), 1023.0 );
_z1=min( max( pArray[2], 0.0 ), 1023.0 );
_w1=min( max( pArray[3], 0.0 ), 3.0 );

instance.v =  ( (uint32_t)_w1 << 30) |
              (((uint32_t)_z1 & 0x3FF) << 20) |
              (((uint32_t)_y1 & 0x3FF) << 10) |
              (((uint32_t)_x1 & 0x3FF));
```

## -see-also

<a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmudec4">XMUDEC4</a>

<a href="/windows/desktop/dxmath/xmudec4-ctor">XMUDEC4 Constructors</a>