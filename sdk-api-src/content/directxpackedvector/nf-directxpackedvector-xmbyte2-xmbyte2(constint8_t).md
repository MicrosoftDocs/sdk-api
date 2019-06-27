---
UID: NF:directxpackedvector.XMBYTE2.XMBYTE2(const int8_t)
title: XMBYTE2::XMBYTE2(const int8_t) (directxpackedvector.h)
author: windows-sdk-content
description: Initializes a new instance of XMBYTE2 from a two-element int8_t array argument.
old-location: 
tech.root: dxmath
ms.assetid: 30912764-5036-4ed9-8c27-249e00fe8eb9
ms.author: windowssdkdev
ms.date: 05/06/2019
ms.keywords: XMBYTE2, XMBYTE2 constructor [DirectX Math Support APIs], XMBYTE2 constructor [DirectX Math Support APIs],XMBYTE2 structure, XMBYTE2 structure [DirectX Math Support APIs],XMBYTE2 constructor, XMBYTE2.XMBYTE2, XMBYTE2.XMBYTE2(), XMBYTE2.XMBYTE2(const int8_t), XMBYTE2::XMBYTE2, XMBYTE2::XMBYTE2(const int8_t), dxmath.xmbyte2_ctor_1
ms.topic: method
f1_keywords: 
 - "directxpackedvector/XMBYTE2.XMBYTE2"
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
 - XMBYTE2.XMBYTE2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# XMBYTE2::XMBYTE2(const int8_t)

## -description

Initializes a new instance of <a href="https://docs.microsoft.com/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmbyte2">XMBYTE2</a> from a two-element <code>int8_t</code> array argument.

This constructor initializes a new instance of <a href="https://docs.microsoft.com/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmbyte2">XMBYTE2</a> from a two-element <code>int8_t</code> array argument.

<div class="alert"><b>Note</b>  This constructor is only available with C++.</div>

## -parameters

### -param pArray

Two-element <code>int8_t</code> array containing the values used to initialize the two components of a new instance of **XMBYTE2**.

## -remarks

The following pseudocode demonstrates the operation of this constructor:

```cpp
XMBYTE2 instance;
instance.x = pArray[0];
instance.y = pArray[1];
```

## -see-also

<a href="https://docs.microsoft.com/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmbyte2">XMBYTE2</a>

<a href="https://docs.microsoft.com/windows/desktop/dxmath/xmbyte2-ctor">XMBYTE2 Constructors</a>
