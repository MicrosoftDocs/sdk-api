---
UID: NF:directxpackedvector.XMHALF2.XMHALF2(const HALF)
title: XMHALF2::XMHALF2(const HALF) (directxpackedvector.h)

description: Initializes a new instance of XMHALF2 from a two element HALF array argument.
old-location: 
tech.root: dxmath
ms.assetid: 4188bae6-91de-4a8a-bcbe-bc7715879f37

ms.date: 05/06/2019
ms.keywords: XMHALF2, XMHALF2 constructor [DirectX Math Support APIs], XMHALF2 constructor [DirectX Math Support APIs],XMHALF2 structure, XMHALF2 structure [DirectX Math Support APIs],XMHALF2 constructor, XMHALF2.XMHALF2, XMHALF2.XMHALF2(), XMHALF2.XMHALF2(const HALF), XMHALF2::XMHALF2, XMHALF2::XMHALF2(const HALF), dxmath.xmhalf2_ctor_1
ms.topic: method
f1_keywords: 
 - "directxpackedvector/XMHALF2.XMHALF2"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DirectXPackedVector.h
api_name:
 - XMHALF2.XMHALF2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# XMHALF2::XMHALF2(const HALF)

## -description

Initializes a new instance of <a href="https://docs.microsoft.com/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmhalf2">XMHALF2</a> from a two element <code>HALF</code> array argument.

This constructor initializes a new instance of **XMHALF2** from a two element <code>HALF</code> array argument.

<div class="alert"><b>Note</b>  This constructor is only available under C++.</div>

## -parameters

### -param pArray

Two element <code>HALF</code> array containing the values used to initialize the two components of a new instance of **XMHALF2**.

## -remarks

The following pseudocode demonstrates the operation of this constructor:
	
```cpp
XMHALF2 instance;
instance.x = pArray[0];
instance.y = pArray[1];
```

## -see-also

<a href="https://docs.microsoft.com/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmhalf2">XMHALF2</a>

<a href="https://docs.microsoft.com/windows/desktop/dxmath/xmhalf2-ctor">XMHALF2 Constructors</a>
