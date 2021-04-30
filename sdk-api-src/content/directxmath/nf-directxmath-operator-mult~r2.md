---
UID: NF:directxmath.operator-mult~r2
title: operator* (multiply by an instance of XMVECTOR)
description: Multiply a floating point value by an instance of XMVECTOR, returning the result a new instance of XMVECTOR.
tech.root: dxmath
helpviewer_keywords: ["operator*"]
ms.assetid: 7c2d058d-ffbd-4698-915a-2375ed25ba28
ms.date: 05/13/2019
ms.keywords: operator*
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
 - operator*
 - directxmath/operator*
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
api_location:
 - directxmath.h
api_name:
 - operator*
---

# operator *(float, XMVECTOR)


## -description

Multiply a floating point value by an instance of **XMVECTOR**, returning the result a new instance of **XMVECTOR**.

The `operator *` multiplies a floating point value against each component of an instance of <a href="/windows/desktop/dxmath/xmvector-data-type">XMVECTOR Data Type</a>, returning a new **XMVECTOR** instance whose components contain the result.

<div class="alert"><b>Note</b>  This operator is only available under C++.</div>

## -parameters

### -param S

Floating point value used as a multiplicand for each component of *V*.

### -param V

**XMVECTOR** instance whose components are multiplicands of this multiplication operation.

## -returns

**XMVECTOR** instance whose components are the product of the multiplication of the corresponding components of *V* by *S*.

## -remarks

The following pseudocode demonstrates the operation of this operator:

```cpp
   XMVECTOR V;
   Float S;
   XMVECTOR Vout;
   Vout.x = S * V1.x;
   Vout.y = S * V1.y;
   Vout.z = S * V1.z;
   Vout.w = S * V1.w;
```

## -see-also

<a href="/windows/desktop/dxmath/xmvector-data-type">XMVECTOR Data Type</a>