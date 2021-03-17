---
UID: NF:directxpackedvector.XMHALF4.XMHALF4(constfloat)
title: XMHALF4::XMHALF4(const float) (directxpackedvector.h)
description: Initializes a new instance of XMHALF4 from a four element float array argument.
helpviewer_keywords: ["XMHALF4","XMHALF4 constructor [DirectX Math Support APIs]","XMHALF4 constructor [DirectX Math Support APIs]","XMHALF4 structure","XMHALF4 structure [DirectX Math Support APIs]","XMHALF4 constructor","XMHALF4.XMHALF4","XMHALF4.XMHALF4()","XMHALF4.XMHALF4(const float)","XMHALF4::XMHALF4","XMHALF4::XMHALF4(const float)","dxmath.xmhalf4_ctor_1"]
old-location: 
tech.root: dxmath
ms.assetid: 0dd6531a-bcc4-4670-8282-e0b26394b07d
ms.date: 05/06/2019
ms.keywords: XMHALF4, XMHALF4 constructor [DirectX Math Support APIs], XMHALF4 constructor [DirectX Math Support APIs],XMHALF4 structure, XMHALF4 structure [DirectX Math Support APIs],XMHALF4 constructor, XMHALF4.XMHALF4, XMHALF4.XMHALF4(), XMHALF4.XMHALF4(const float), XMHALF4::XMHALF4, XMHALF4::XMHALF4(const float), dxmath.xmhalf4_ctor_1
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
 - XMHALF4::XMHALF4
 - directxpackedvector/XMHALF4::XMHALF4
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
 - XMHALF4.XMHALF4
---

# XMHALF4::XMHALF4(const float)


## -description

Initializes a new instance of <a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmhalf4">XMHALF4</a> from a four element <code>float</code> array argument.

This constructor initializes a new instance of **XMHALF4** from a four element <code>float</code> array argument.

<div class="alert"><b>Note</b>  This constructor is only available under C++.</div>

## -parameters

### -param pArray

Four element <code>float</code> array containing the values used to initialize the four components of a new instance of **XMHALF4**.

## -remarks

If the magnitude of one of the members of *pArray* cannot be represented by the **HALF** type, the corresponding member of the new instance of **XMHALF4** will be infinity for a 16-bit integer (+0x7FFF).

The following pseudocode demonstrates the operation of this constructor using the XNA Math *XMConvertFloatToHalf* function:

```cpp
XMHALF4 instance;

instance.x = XMConvertFloatToHalf(pArray[0]);
instance.y = XMConvertFloatToHalf(pArray[1]);
instance.z = XMConvertFloatToHalf(pArray[2]);
instance.w = XMConvertFloatToHalf(pArray[3]);
```

## -see-also

<a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmhalf4">XMHALF4</a>

<a href="/windows/desktop/dxmath/xmhalf4-ctor">XMHALF4 Constructors</a>