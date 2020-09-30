---
UID: NF:directxmath.operator-mult
title: operator*
description: Multiplies one instance of XMVECTOR by a second instance, returning the result in a third instance.
tech.root: dxmath
helpviewer_keywords: ["operator*"]
ms.assetid: 27e77bf4-0520-47bf-b2a9-884cff1b8944
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
 - 
api_location:
 - directxmath.h
api_name:
 - operator*
---

# XMVECTOR::operator * (XMVECTOR,XMVECTOR)


## -description

Multiplies one instance of **XMVECTOR** by a second instance, returning the result in a third instance.

The `operator *` multiplies each component of an instance of <a href="/windows/desktop/dxmath/xmvector-data-type">XMVECTOR Data Type</a> by the corresponding component in a second instance of **XMVECTOR**, returning a new **XMVECTOR** instance containing the result.

<div class="alert"><b>Note</b>  This operator is only available under C++.</div>

## -parameters

### -param V1

**XMVECTOR** instance whose components provide one set of multiplicands for this multiplication operation.

### -param V2

**XMVECTOR** instance whose components provide one set of multiplicands for this multiplication operation.

## -returns

**XMVECTOR** instance whose components are the product of the multiplication of the corresponding components of *V1* by *V2*.

## -remarks

The following pseudocode demonstrates the operation of this operator:

```cpp
   XMVECTOR V;
   Float S;
   XMVECTOR Vout;
   Vout.x = V1.x * V2.x;
   Vout.y = V1.y * V2.y;
   Vout.z = V1.z * V2.z;
   Vout.w = V1.w * V2.w;
```

## -see-also

<a href="/windows/desktop/dxmath/xmvector-data-type">XMVECTOR Data Type</a>