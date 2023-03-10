---
UID: NF:directxmath.XMUINT2.XMUINT2(constuint32_t)
title: XMUINT2::XMUINT2(const uint32_t) (directxmath.h)
description: Initializes a new instance of XMUINT2 from a two element uint32_t array argument.
helpviewer_keywords: ["XMUINT2","XMUINT2 constructor [DirectX Math Support APIs]","XMUINT2 constructor [DirectX Math Support APIs]","XMUINT2 structure","XMUINT2 structure [DirectX Math Support APIs]","XMUINT2 constructor","XMUINT2.XMUINT2","XMUINT2.XMUINT2()","XMUINT2.XMUINT2(const uint32_t)","XMUINT2::XMUINT2","XMUINT2::XMUINT2(const uint32_t)","dxmath.xmuint2_ctor_1"]
old-location: 
tech.root: dxmath
ms.assetid: 412fe549-c4b1-48c7-bbaf-a914d7c1e0a1
ms.date: 05/13/2019
ms.keywords: XMUINT2, XMUINT2 constructor [DirectX Math Support APIs], XMUINT2 constructor [DirectX Math Support APIs],XMUINT2 structure, XMUINT2 structure [DirectX Math Support APIs],XMUINT2 constructor, XMUINT2.XMUINT2, XMUINT2.XMUINT2(), XMUINT2.XMUINT2(const uint32_t), XMUINT2::XMUINT2, XMUINT2::XMUINT2(const uint32_t), dxmath.xmuint2_ctor_1
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - XMUINT2::XMUINT2
 - directxmath/XMUINT2::XMUINT2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DirectXMath.h
api_name:
 - XMUINT2.XMUINT2
---

# XMUINT2::XMUINT2(const uint32_t)


## -description

Initializes a new instance of <a href="/windows/desktop/direct3dhlsl/xmuint2">XMUINT2</a> from a two element <code>uint32_t</code> array argument.

This constructor initializes a new instance of **XMUINT2** from a two element <code>uint32_t</code> array argument.

<div class="alert"><b>Note</b>  This constructor is only available under C++.</div>

## -parameters

### -param pArray

Two element **uint32_t** array containing the values used to initialize the two components of a new instance of **XMUINT2**.

## -remarks

```cpp
XMUINT2 instance;
instance.x = pArray[0];
instance.y = pArray[1];
instance.z = pArray[2];
instance.w = pArray[3];
```

## -see-also

<a href="/windows/desktop/direct3dhlsl/xmuint2">XMUINT2</a>

<a href="/windows/desktop/api/directxmath/nf-directxmath-xmuint2-xmuint2(constuint32_t)">XMUINT2 Constructors</a>