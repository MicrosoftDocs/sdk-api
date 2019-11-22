---
UID: NF:directxmath.operator-sub
title: operator-
description: Computes the negation of an XMVECTOR instance.
ms.assetid: 96195aef-4e7b-4819-92a2-96379bc9f506

ms.date: 05/13/2019
ms.keywords: operator-
ms.topic: language-reference
f1_keywords: 
 - "directxmath/operator-"
dev_langs:
 - c++
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
topic_type:
 - apiref
api_type:
 - 
api_location:
 - directxmath.h
api_name:
 - operator-
---

# operator -(XMVECTOR)

## -description

Computes the negation of an **XMVECTOR** instance.

The `operator -` takes an instance of <a href="https://docs.microsoft.com/windows/desktop/dxmath/xmvector-data-type">XMVECTOR Data Type</a> and returns a new instance of **XMVECTOR**, with each component negated.

<div class="alert"><b>Note</b>  This operator is only available under C++.</div>

## -parameters

### -param V

Vector whose components are to have their signs changed.

## -returns

Vector whose components are the negation of *V*.

## -remarks

The following pseudocode demonstrates the operation of this operator:

```cpp
   XMVECTOR V;
   XMVECTOR Vout;
   Vout.x = - V.x;
   Vout.y = - V.y;
   Vout.z = - V.z;
   Vout.w = - V.w;
```

## -see-also

<a href="https://docs.microsoft.com/windows/desktop/dxmath/xmvector-data-type">XMVECTOR Data Type</a>
