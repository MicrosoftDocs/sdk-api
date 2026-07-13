---
UID: NF:directxmath.XMFLOAT3X4A.operator-assign(XMFLOAT3X4A&&)
title: XMFLOAT3X4A::operator=
ms.date: 11/8/2019
targetos: Windows
description: Move assignment operator for **XMFLOAT3X4A**. Moves the argument's vector component data into the current instance of **XMFLOAT3X4A**.
tech.root: dxmath
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
req.target-min-winverclnt: Windows Build 22000
req.target-min-winversvr: Windows Build 22000
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
api_location:
 - directxmath.h
api_name:
 - XMFLOAT3X4A::operator=
f1_keywords:
 - XMFLOAT3X4A::operator=
 - directxmath/XMFLOAT3X4A::operator=
dev_langs:
 - c++
---

## -description

Move assignment operator for **XMFLOAT3X4A**. Moves the argument's vector component data into the current instance of **XMFLOAT3X4A**.

## -parameters

### -param unnamedParam1

Type: **XMFLOAT3X4A &&**

An rvalue reference to an **XMFLOAT3X4A** value whose vector component data the operator should move into the current instance of **XMFLOAT3X4A**.

## -returns

Type: **XMFLOAT3X4A &**

An lvalue reference to the current instance of **XMFLOAT3X4A**, after moving *arg1* into it.

## -see-also

[XMFLOAT3X4A structure](./ns-directxmath-xmfloat3x4a.md)
