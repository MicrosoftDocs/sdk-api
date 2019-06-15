---
UID: NF:directxmath.XMUINT4.XMUINT4(const uint32_t)
title: XMUINT4::XMUINT4(const uint32_t) (directxmath.h)
author: windows-sdk-content
description: Initializes a new instance of XMUINT4 from a four element uint32_t array argument.
old-location: 
tech.root: dxmath
ms.assetid: 015b6b50-e749-452e-b05e-a5d18c29fea2
ms.author: windowssdkdev
ms.date: 05/13/2019
ms.keywords: XMUINT4, XMUINT4 constructor [DirectX Math Support APIs], XMUINT4 constructor [DirectX Math Support APIs],XMUINT4 structure, XMUINT4 structure [DirectX Math Support APIs],XMUINT4 constructor, XMUINT4.XMUINT4, XMUINT4.XMUINT4(), XMUINT4.XMUINT4(const uint32_t), XMUINT4::XMUINT4, XMUINT4::XMUINT4(const uint32_t), dxmath.xmuint4_ctor_1
ms.topic: method
f1_keywords: ["directxmath/XMUINT4.XMUINT4"]
req.header: directxmath.h
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
req.namespace: Use DirectX.
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
 - DirectXMath.h
api_name:
 - XMUINT4.XMUINT4
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# XMUINT4::XMUINT4(const uint32_t)

## -description

Initializes a new instance of <a href="https://docs.microsoft.com/windows/desktop/api/directxmath/ns-directxmath-xmuint4">XMUINT4</a> from a four element <code>uint32_t</code> array argument.

This constructor initializes a new instance of **XMUINT4** from a four element <code>uint32_t</code> array argument.

<div class="alert"><b>Note</b>  This constructor is only available under C++.</div>

## -parameters

### -param pArray

Four element **uint32_t** array containing the values used to initialize the four components of a new instance of **XMUINT4**.

## -remarks

The following pseudocode demonstrates the operation of this constructor:

```cpp
XMUINT4 instance;
instance.x = pArray[0];
instance.y = pArray[1];
instance.z = pArray[2];
instance.w = pArray[3];
```

## -see-also

<a href="https://docs.microsoft.com/windows/desktop/api/directxmath/ns-directxmath-xmuint4">XMUINT4</a>

<a href="https://docs.microsoft.com/windows/desktop/api/directxmath/nf-directxmath-xmuint4-xmuint4(constuint32_t)">XMUINT4 Constructors</a>
