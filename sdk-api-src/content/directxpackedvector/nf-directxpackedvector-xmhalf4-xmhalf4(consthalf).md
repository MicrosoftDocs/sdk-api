---
UID: NF:directxpackedvector.XMHALF4.XMHALF4(constHALF)
title: XMHALF4::XMHALF4(const HALF) (directxpackedvector.h)
description: Initializes a new instance of XMHALF4 from a four element HALF array argument.
helpviewer_keywords: ["XMHALF4","XMHALF4 constructor [DirectX Math Support APIs]","XMHALF4 constructor [DirectX Math Support APIs]","XMHALF4 structure","XMHALF4 structure [DirectX Math Support APIs]","XMHALF4 constructor","XMHALF4.XMHALF4","XMHALF4.XMHALF4()","XMHALF4.XMHALF4(const HALF)","XMHALF4::XMHALF4","XMHALF4::XMHALF4(const HALF)","dxmath.xmhalf4_ctor_1"]
old-location: 
tech.root: dxmath
ms.assetid: 9ee7c969-064a-4b66-8114-ab97a920b4fc
ms.date: 05/06/2019
ms.keywords: XMHALF4, XMHALF4 constructor [DirectX Math Support APIs], XMHALF4 constructor [DirectX Math Support APIs],XMHALF4 structure, XMHALF4 structure [DirectX Math Support APIs],XMHALF4 constructor, XMHALF4.XMHALF4, XMHALF4.XMHALF4(), XMHALF4.XMHALF4(const HALF), XMHALF4::XMHALF4, XMHALF4::XMHALF4(const HALF), dxmath.xmhalf4_ctor_1
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

# XMHALF4::XMHALF4(const HALF)


## -description

Initializes a new instance of <a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmhalf4">XMHALF4</a> from a four element <code>HALF</code> array argument.

This constructor initializes a new instance of **XMHALF4** from a from a four element <code>XMHALF4</code> array argument.

<div class="alert"><b>Note</b>  This constructor is only available under C++.</div>

## -parameters

### -param pArray

Four element **HALF** array containing the values used to initialize the four components of a new instance of **XMHALF4**.

## -remarks

The following pseudocode demonstrates the operation of this constructor:

```cpp
XMHALF4 instance;
instance.x = pArray[0];
instance.y = pArray[1];
instance.z = pArray[2];
instance.w = pArray[3];
```

## -see-also

<a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmhalf4">XMHALF4</a>

<a href="/windows/desktop/dxmath/xmhalf4-ctor">XMHALF4 Constructors</a>