---
UID: NF:directxmath.operator-mult-assign~r1
title: operator*= (multiply)
description: Multiplies an XMVECTOR instance by a floating point value and returns a reference to the updated instance.
tech.root: dxmath
helpviewer_keywords: ["operator*="]
ms.assetid: 4e858092-8a1e-4c71-9f90-61a9c0f13544
ms.date: 05/13/2019
ms.keywords: operator*=
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
 - operator*=
 - directxmath/operator*=
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
api_location:
 - directxmath.h
api_name:
 - operator*=
---

# operator *=(XMVECTOR&, float)


## -description

Multiplies an **XMVECTOR** instance by a floating point value and returns a reference to the updated instance.

The `operator *=` multiplies each component of the current instance of <a href="/windows/desktop/dxmath/xmvector-data-type">XMVECTOR Data Type</a> by a specified floating point value, returning a reference to the updated current instance.

<div class="alert"><b>Note</b>  This operator is only available under C++.</div>

## -parameters

### -param V

Reference to current instance of **XMVECTOR**.

### -param S

Floating point multiplicand.

## -returns

Reference to the updated current instance of **XMVECTOR**.

## -remarks

The following pseudocode demonstrates the operation of this operator:

```cpp
   XMVECTOR V;
   V.x = V.x * S;
   V.y = V.y * S;
   V.z = V.z * S;
   V.w = V.w * S;
```

## -see-also

<a href="/windows/desktop/dxmath/xmvector-data-type">XMVECTOR Data Type</a>