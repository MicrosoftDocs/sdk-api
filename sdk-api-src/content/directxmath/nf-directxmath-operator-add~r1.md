---
UID: NF:directxmath.operator-add~r1
title: operator+ (add)
description: Adds two instances of **XMVECTOR**, returning the result in a new instance.
tech.root: dxmath
helpviewer_keywords: ["operator+"]
ms.assetid: 24dc38ff-fa79-4fba-b7fb-594722c5c967
ms.date: 05/13/2019
ms.keywords: operator+
targetos: Windows
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: directxmath.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
f1_keywords:
 - operator+
 - directxmath/operator+
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
api_location:
 - directxmath.h
api_name:
 - operator+
---

# XMVECTOR::operator + (XMVECTOR,XMVECTOR)


## -description

Adds two instances of **XMVECTOR**, returning the result in a new instance.

The `operator +` adds each component of two instances of <a href="/windows/desktop/dxmath/xmvector-data-type">XMVECTOR Data Type</a>, and then returns the result in a new **XMVECTOR** instance.

<div class="alert"><b>Note</b>  This operator is only available under C++.</div>

## -parameters

### -param V1

Instance of **XMVECTOR** whose components added to those of *V2*.

### -param V2

Instance of **XMVECTOR** whose components added to those of *V1*.

## -returns

**XMVECTOR** instance whose components are the sum of the corresponding components of *V1* and *V2*.

## -remarks

The following pseudocode demonstrates the operation of this operator:

```cpp
   XMVECTOR V1;
   XMVECTOR V2;
   XMVECTOR Vout;
   Vout.x = V1.x + V2.x;
   Vout.y = V1.y + V2.y;
   Vout.z = V1.z + V2.z;
   Vout.w = V1.w + V2.w;
```

## -see-also

<a href="/windows/desktop/dxmath/xmvector-data-type">XMVECTOR Data Type</a>