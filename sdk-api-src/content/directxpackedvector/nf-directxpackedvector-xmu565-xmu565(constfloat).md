---
UID: NF:directxpackedvector.XMU565.XMU565(constfloat)
title: XMU565::XMU565(const float) (directxpackedvector.h)
description: Initializes a new instance of XMU565 from a three element float array.
helpviewer_keywords: ["XMU565","XMU565 constructor [DirectX Math Support APIs]","XMU565 constructor [DirectX Math Support APIs]","XMU565 structure","XMU565 structure [DirectX Math Support APIs]","XMU565 constructor","XMU565.XMU565","XMU565.XMU565()","XMU565.XMU565(const float)","XMU565::XMU565","XMU565::XMU565(const float)","dxmath.xmu565_ctor_1"]
old-location: 
tech.root: dxmath
ms.assetid: 5b3d6816-55a0-4f56-9b1c-ffe8899c5477
ms.date: 05/06/2019
ms.keywords: XMU565, XMU565 constructor [DirectX Math Support APIs], XMU565 constructor [DirectX Math Support APIs],XMU565 structure, XMU565 structure [DirectX Math Support APIs],XMU565 constructor, XMU565.XMU565, XMU565.XMU565(), XMU565.XMU565(const float), XMU565::XMU565, XMU565::XMU565(const float), dxmath.xmu565_ctor_1
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

# XMU565::XMU565(const float)


## -description

Initializes a new instance of <a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmu565">XMU565</a> from a three element <code>float</code> array.

This constructor initializes a new instance of **XMU565** from a three element <code>float</code> array.

<div class="alert"><b>Note</b>  This is only available for C++ based development.</div>

## -parameters

### -param pArray

Three element floating point array containing the values used to initialize the x-, y- and z-components of a new instance of XMU565.

## -remarks

Array elements and the **_w** argument are mapped to the vector components of a new instance of XMU565 as follows:

| XMU565 Member | Argument | Range |
|---------------|----------|-------|
| x | pArray[0] | 0.0, 31.0 |
| y | pArray[1] | 0.0, 63.0 |
| z | pArray[2] | 0.0, 31.0 |

Arguments to the constructors will be clamped to the permitted range prior to assignment to the appropriate member of XMU565.

The following pseudocode demonstrates the operation of this constructor, which takes union of the three components of the XMU565vector with an instance of **uint16_t** in the definition of the structure:

```cpp
XMU565 instance;
_x1=min( max( pArray[0], 0.0 ), 31.0);
_y1=min( max( pArray[1], 0.0 ), 63.0 );
_z1=min( max( pArray[2], 0.0 ), 31.0 );

instance.v= ((z & 0x1F) << 11) |
            ((y & 0x3F) << 5) |
            ((x & 0x1F));
```

## -see-also

<a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmu565">XMU565</a>

<a href="/windows/desktop/dxmath/xmu565-ctor">XMU565 Constructors</a>