---
UID: NF:directxmath.operator-sub~r1
title: operator- (subtract)
description: Subtracts one instance of XMVECTOR from a second instance, returning the result in a new instance of XMVECTOR.
tech.root: dxmath
helpviewer_keywords: ["operator-"]
ms.assetid: d41c1951-c696-4132-98fb-d403f26c4d3b
ms.date: 05/13/2019
ms.keywords: operator-
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
 - operator-
 - directxmath/operator-
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
api_location:
 - directxmath.h
api_name:
 - operator-
---

# operator -(XMVECTOR, XMVECTOR)


## -description

Subtracts one instance of **XMVECTOR** from a second instance, returning the result in a new instance of **XMVECTOR**.

The `operator -` subtracts each component of an instance of <a href="/windows/desktop/dxmath/xmvector-data-type">XMVECTOR Data Type</a> from each component of another instance of **XMVECTOR**, returning a new **XMVECTOR** instance containing the result.

<div class="alert"><b>Note</b>  This operator is only available under C++.</div>

## -parameters

### -param V1

**XMVECTOR** instance whose components are the minuends of the subtraction operation.

### -param V2

**XMVECTOR** instance whose components are the subtrahends of the subtraction operation.

## -returns

**XMVECTOR** instance whose components are the result of subtracting of each component of *V2* from each corresponding component of *V1*.

## -remarks

The following pseudocode demonstrates the operation of this operator:

```cpp
   XMVECTOR V1;
   XMVECTOR V2;
   XMVECTOR Vout;
   Vout.x = V1.x - V2.x;
   Vout.y = V1.y - V2.y;
   Vout.z = V1.z - V2.z;
   Vout.w = V1.w - V2.w;
```

## -see-also

<a href="/windows/desktop/dxmath/xmvector-data-type">XMVECTOR Data Type</a>