---
UID: NF:directxpackedvector.XMSHORTN4.XMSHORTN4(constint16_t)
title: XMSHORTN4::XMSHORTN4(const int16_t) (directxpackedvector.h)
description: Initializes a new instance of XMSHORTN4 from a four element int16_t array argument.
helpviewer_keywords: ["XMSHORTN4","XMSHORTN4 constructor [DirectX Math Support APIs]","XMSHORTN4 constructor [DirectX Math Support APIs]","XMSHORTN4 structure","XMSHORTN4 structure [DirectX Math Support APIs]","XMSHORTN4 constructor","XMSHORTN4.XMSHORTN4","XMSHORTN4.XMSHORTN4()","XMSHORTN4.XMSHORTN4(const int16_t)","XMSHORTN4::XMSHORTN4","XMSHORTN4::XMSHORTN4(const int16_t)","dxmath.xmshortn4_ctor_1"]
old-location: 
tech.root: dxmath
ms.assetid: c9210140-2e89-4269-95a7-c43341606660
ms.date: 05/06/2019
ms.keywords: XMSHORTN4, XMSHORTN4 constructor [DirectX Math Support APIs], XMSHORTN4 constructor [DirectX Math Support APIs],XMSHORTN4 structure, XMSHORTN4 structure [DirectX Math Support APIs],XMSHORTN4 constructor, XMSHORTN4.XMSHORTN4, XMSHORTN4.XMSHORTN4(), XMSHORTN4.XMSHORTN4(const int16_t), XMSHORTN4::XMSHORTN4, XMSHORTN4::XMSHORTN4(const int16_t), dxmath.xmshortn4_ctor_1
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
 - XMSHORTN4::XMSHORTN4
 - directxpackedvector/XMSHORTN4::XMSHORTN4
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
 - XMSHORTN4.XMSHORTN4
---

# XMSHORTN4::XMSHORTN4(const int16_t)


## -description

Initializes a new instance of <a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmshortn4">XMSHORTN4</a> from a four element <code>int16_t</code> array argument.

This constructor initializes a new instance of **XMSHORTN4** from a four element <code>int16_t</code> array argument.

<div class="alert"><b>Note</b>  This constructor is only available under C++.</div>

## -parameters

### -param pArray

Four element <code>int16_t</code> array containing the values used to initialize the four components of a new instance of **XMSHORTN4**.

## -remarks

Input values are not normalized. The following pseudocode demonstrates the operation of this constructor:

```cpp
XMSHORTN4 instance;
instance.x = pArray[0];
instance.y = pArray[1];
instance.z = pArray[2];
instance.w = pArray[3];
```

## -see-also

<a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmshortn4">XMSHORTN4</a>

<a href="/windows/desktop/dxmath/xmshortn4-ctor">XMSHORTN4 Constructors</a>