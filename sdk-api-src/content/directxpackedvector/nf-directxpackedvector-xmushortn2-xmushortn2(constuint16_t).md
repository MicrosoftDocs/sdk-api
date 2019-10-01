---
UID: NF:directxpackedvector.XMUSHORTN2.XMUSHORTN2(const uint16_t)
title: XMUSHORTN2::XMUSHORTN2(const uint16_t) (directxpackedvector.h)
author: windows-sdk-content
description: Initializes a new instance of XMUSHORTN2 from a two element uint16_t array argument.
old-location: 
tech.root: dxmath
ms.assetid: 15aeb82d-2262-4727-b591-47f9435bf6fd
ms.author: windowssdkdev
ms.date: 05/06/2019
ms.keywords: XMUSHORTN2, XMUSHORTN2 constructor [DirectX Math Support APIs], XMUSHORTN2 constructor [DirectX Math Support APIs],XMUSHORTN2 structure, XMUSHORTN2 structure [DirectX Math Support APIs],XMUSHORTN2 constructor, XMUSHORTN2.XMUSHORTN2, XMUSHORTN2.XMUSHORTN2(), XMUSHORTN2.XMUSHORTN2(const uint16_t), XMUSHORTN2::XMUSHORTN2, XMUSHORTN2::XMUSHORTN2(const uint16_t), dxmath.xmushortn2_ctor_1
ms.topic: method
f1_keywords: 
 - "directxpackedvector/XMUSHORTN2.XMUSHORTN2"
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
 - XMUSHORTN2.XMUSHORTN2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# XMUSHORTN2::XMUSHORTN2(const uint16_t)

## -description

Initializes a new instance of <a href="https://docs.microsoft.com/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmushortn2">XMUSHORTN2</a> from a two element <code>uint16_t</code> array argument.

This constructor initializes a new instance of **XMUSHORTN2** from a from a two element <code>uint16_t</code> array argument.

<div class="alert"><b>Note</b>  This constructor is only available under C++.</div>

## -parameters

### -param pArray

Two element **uint16_t** array containing the values used to initialize the two components of a new instance of XMUSHORTN2.

## -remarks

Input values are not normalized. The following pseudocode demonstrates the operation of this constructor:

```cpp
XMUSHORTN2 instance;
instance.x = pArray[0];
instance.y = pArray[1];
```

## -see-also

<a href="https://docs.microsoft.com/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmushortn2">XMUSHORTN2</a>

<a href="https://docs.microsoft.com/windows/desktop/dxmath/xmushortn2-ctor">XMUSHORTN2 Constructors</a>
