---
UID: NF:directxmath.operator-div-assign
title: operator/=
description: Divides one XMVECTOR instance by a second instance, returning a reference to the updated initial instance.
tech.root: dxmath
helpviewer_keywords: ["operator/="]
ms.assetid: 75ec577b-7ed3-4b0b-a285-86aa443c8355
ms.date: 05/13/2019
ms.keywords: operator/=
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
 - operator/=
 - directxmath/operator/=
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
api_location:
 - directxmath.h
api_name:
 - operator/=
---

# XMVECTOR::operator /= (XMVECTOR&,XMVECTOR)


## -description

Divides one **XMVECTOR** instance by a second instance, returning a reference to the updated initial instance.

The `operator /=` divides each component of the current instance of <a href="/windows/desktop/dxmath/xmvector-data-type">XMVECTOR Data Type</a> by the corresponding component in a second specified instance of **XMVECTOR**, returning a reference to the updated initial instance.

<div class="alert"><b>Note</b>  This operator is only available under C++.</div>

## -parameters

### -param V1

Reference to current instance of **XMVECTOR**.

### -param V2

**XMVECTOR** instance whose components are to be divisors.

## -returns

Reference to the updated current instance of **XMVECTOR** containing the result of the division operation.

## -remarks

The following pseudocode demonstrates the operation of this operator:

```cpp
   XMVECTOR V1;
   XMVECTOR V2;
   V1.x = V1.x / V2.x;
   V1.y = V1.y / V2.y;
   V1.z = V1.z / V2.z;
   V1.w = V1.w / V2.w;
```

## -see-also

<a href="/windows/desktop/dxmath/xmvector-data-type">XMVECTOR Data Type</a>