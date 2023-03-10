---
UID: NF:directxmath.operator-mult~r1
title: operator* (multiply)
description: Multiply an instance of XMVECTOR by a floating point value, returning the result a new instance of XMVECTOR.
tech.root: dxmath
helpviewer_keywords: ["operator*"]
ms.assetid: ebfb61d9-0b98-4e89-a196-bb43881c7252
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

# operator *(XMVECTOR, float)


## -description

Multiply an instance of **XMVECTOR** by a floating point value, returning the result a new instance of **XMVECTOR**.

The `operator *` multiplies each component of an instance of <a href="/windows/desktop/dxmath/xmvector-data-type">XMVECTOR Data Type</a> by a floating point value, returning a new **XMVECTOR** instance whose components contain the result.

<div class="alert"><b>Note</b>  This operator is only available under C++.</div>

## -parameters

### -param V

**XMVECTOR** instance whose components are multiplicands of this multiplication operation.

### -param S

Floating point value used as a multiplicand for each component of *V*.

## -returns

**XMVECTOR** instance whose components are the product of the multiplication of the corresponding components of *V* by *S*.

## -remarks

The following pseudocode demonstrates the operation of this operator:

```cpp
   XMVECTOR V;
   Float S;
   XMVECTOR Vout;
   Vout.x = V1.x * S;
   Vout.y = V1.y * S;
   Vout.z = V1.z * S;
   Vout.w = V1.w * S;
```

## -see-also

<a href="/windows/desktop/dxmath/xmvector-data-type">XMVECTOR Data Type</a>