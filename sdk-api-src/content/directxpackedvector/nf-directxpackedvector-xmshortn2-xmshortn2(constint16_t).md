---
UID: NF:directxpackedvector.XMSHORTN2.XMSHORTN2(constint16_t)
title: XMSHORTN2::XMSHORTN2(const int16_t) (directxpackedvector.h)
description: Initializes a new instance of XMSHORTN2 from a two element int16_t array argument.
helpviewer_keywords: ["XMSHORTN2","XMSHORTN2 constructor [DirectX Math Support APIs]","XMSHORTN2 constructor [DirectX Math Support APIs]","XMSHORTN2 structure","XMSHORTN2 structure [DirectX Math Support APIs]","XMSHORTN2 constructor","XMSHORTN2.XMSHORTN2","XMSHORTN2.XMSHORTN2()","XMSHORTN2.XMSHORTN2(const int16_t)","XMSHORTN2::XMSHORTN2","XMSHORTN2::XMSHORTN2(const int16_t)","dxmath.xmshortn2_ctor_1"]
old-location: 
tech.root: dxmath
ms.assetid: 1a83878c-8ac6-4256-b962-01fac390daf8
ms.date: 05/06/2019
ms.keywords: XMSHORTN2, XMSHORTN2 constructor [DirectX Math Support APIs], XMSHORTN2 constructor [DirectX Math Support APIs],XMSHORTN2 structure, XMSHORTN2 structure [DirectX Math Support APIs],XMSHORTN2 constructor, XMSHORTN2.XMSHORTN2, XMSHORTN2.XMSHORTN2(), XMSHORTN2.XMSHORTN2(const int16_t), XMSHORTN2::XMSHORTN2, XMSHORTN2::XMSHORTN2(const int16_t), dxmath.xmshortn2_ctor_1
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

# XMSHORTN2::XMSHORTN2(const int16_t)


## -description

Initializes a new instance of <a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmshortn2">XMSHORTN2</a> from a two element <code>int16_t</code> array argument.

This constructor initializes a new instance of **XMSHORTN2** from a two element <code>int16_t</code> array argument.

<div class="alert"><b>Note</b>  This constructor is only available under C++.</div>

## -parameters

### -param pArray

Two element <code>int16_t</code> array containing the values used to initialize the two components of a new instance of **XMSHORTN2**.

## -remarks

Input values are not normalized. The following pseudocode demonstrates the operation of this constructor:

```cpp
XMSHORTN2 instance;
instance.x = pArray[0];
instance.y = pArray[1];
```

## -see-also

<a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmshortn2">XMSHORTN2</a>

<a href="/windows/desktop/dxmath/xmshortn2-ctor">XMSHORTN2 Constructors</a>