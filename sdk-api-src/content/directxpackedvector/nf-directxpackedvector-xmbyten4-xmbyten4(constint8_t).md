---
UID: NF:directxpackedvector.XMBYTEN4.XMBYTEN4(constint8_t)
title: XMBYTEN4::XMBYTEN4(const int8_t) (directxpackedvector.h)
description: Initializes a new instance of XMBYTEN4 from a four element int8_t array argument.
helpviewer_keywords: ["XMBYTEN4","XMBYTEN4 constructor [DirectX Math Support APIs]","XMBYTEN4 constructor [DirectX Math Support APIs]","XMBYTEN4 structure","XMBYTEN4 structure [DirectX Math Support APIs]","XMBYTEN4 constructor","XMBYTEN4.XMBYTEN4","XMBYTEN4.XMBYTEN4()","XMBYTEN4.XMBYTEN4(const int8_t)","XMBYTEN4::XMBYTEN4","XMBYTEN4::XMBYTEN4(const int8_t)","dxmath.xmbyten4_ctor_1"]
old-location: 
tech.root: dxmath
ms.assetid: d1ca7edc-3f93-4100-bc64-de560d052ad5
ms.date: 05/06/2019
ms.keywords: XMBYTEN4, XMBYTEN4 constructor [DirectX Math Support APIs], XMBYTEN4 constructor [DirectX Math Support APIs],XMBYTEN4 structure, XMBYTEN4 structure [DirectX Math Support APIs],XMBYTEN4 constructor, XMBYTEN4.XMBYTEN4, XMBYTEN4.XMBYTEN4(), XMBYTEN4.XMBYTEN4(const int8_t), XMBYTEN4::XMBYTEN4, XMBYTEN4::XMBYTEN4(const int8_t), dxmath.xmbyten4_ctor_1
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
 - XMBYTEN4::XMBYTEN4
 - directxpackedvector/XMBYTEN4::XMBYTEN4
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
 - XMBYTEN4.XMBYTEN4
---

# XMBYTEN4::XMBYTEN4(const int8_t)


## -description

Initializes a new instance of <a href="/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmbyten4">XMBYTEN4</a> from a four element <code>int8_t</code> array argument.

This constructor initializes a new instance of **XMBYTEN4** from a four element <code>int8_t</code> array argument.

<div class="alert"><b>Note</b>  This constructor is only available under C++.</div>

## -parameters

### -param pArray

Four element <code>int8_t</code> array containing the values used to initialize the four components of a new instance of **XMBYTEN4**.

## -remarks

Input values are not normalized. The following pseudocode demonstrates the operation of this constructor:

```cpp
XMBYTEN4 instance;
instance.x = pArray[0];
instance.y = pArray[1];
instance.z = pArray[2];
instance.w = pArray[3];
```

## -see-also

<a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmbyten4">XMBYTEN4</a>

<a href="/windows/desktop/dxmath/xmbyten4-ctor">XMBYTEN4 Constructors</a>
