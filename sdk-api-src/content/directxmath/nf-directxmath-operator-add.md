---
UID: NF:directxmath.operator-add
title: operator+
description: Performance an identity operation on an XMVECTOR instance.
tech.root: dxmath
helpviewer_keywords: ["operator+"]
ms.assetid: 746972ab-796a-4abd-8a96-7a4f8ccdd808
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

# XMVECTOR::operator + (XMVECTOR)


## -description

Performance an identity operation on an **XMVECTOR** instance.

The `operator +` takes an instance of <a href="/windows/desktop/dxmath/xmvector-data-type">XMVECTOR Data Type</a> and returns a new instance of XMVECTOR, with an identity operator applied to each component.

<div class="alert"><b>Note</b>  This operator is only available under C++.</div>

## -parameters

### -param V

Vector whose components are to be acted on by an identify operation.

## -returns

Vector whose components are the result of the identity operation performed on *V*.

## -remarks

## -see-also

<a href="/windows/desktop/dxmath/xmvector-data-type">XMVECTOR Data Type</a>