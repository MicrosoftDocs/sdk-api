---
UID: NF:directxmath.operator-add-assign
title: operator+=
description: Adds a floating point value to an XMVECTOR instance, and returns a reference to the updated instance.
tech.root: dxmath
helpviewer_keywords: ["operator+="]
ms.assetid: 2e3873c5-2871-49b5-ac2d-4da0d84aa169
ms.date: 05/13/2019
ms.keywords: operator+=
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
 - operator+=
 - directxmath/operator+=
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
api_location:
 - directxmath.h
api_name:
 - operator+=
---

# XMVECTOR::operator +=


## -description

Adds a floating point value to an **XMVECTOR** instance, and returns a reference to the updated instance.

The `operator +=` adds a specified floating point value to each component of the current instance of <a href="/windows/desktop/dxmath/xmvector-data-type">XMVECTOR Data Type</a>, returning a reference to the updated current instance.

<div class="alert"><b>Note</b>  This operator is only available under C++.</div>

## -parameters

### -param V1

Reference to current instance of **XMVECTOR**.

### -param V2

**XMVECTOR** instance whose components are to be added to the component of *V1*.

## -returns

Reference to the updated current instance of **XMVECTOR**.

## -remarks

The following pseudocode demonstrates the operation of this operator:

```cpp
   XMVECTOR V;
   V1.x = V1.x + V2.x;
   V1.y = V1.y + V2.y;
   V1.z = V1.z + V2.z;
   V1.w = V1.w + V2.w;
```

## -see-also

<a href="/windows/desktop/dxmath/xmvector-data-type">XMVECTOR Data Type</a>