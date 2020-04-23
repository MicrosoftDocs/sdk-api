---
UID: NF:directxmath.XMFLOAT3X4A.operator-assign(XMFLOAT3X4A &&)
title: XMFLOAT3X4A::operator=
ms.date: 11/8/2019
ms.topic: language-reference
targetos: Windows
description: Assigns the **XMFLOAT3X4A** argument's vector component data to the current instance of **XMFLOAT3X4A**.
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
 - XMFLOAT3X4A::operator=
f1_keywords:
 - directxmath/XMFLOAT3X4A::operator=
dev_langs:
 - c++
---

## -description

Assigns the **XMFLOAT3X4A** argument's vector component data to the current instance of **XMFLOAT3X4A**.

## -parameters

### -param arg1

Type: **XMFLOAT3X4A &&**

An rvalue reference to an **XMFLOAT3X4A** value whose vector component data the operator should copy into the current **XMFLOAT3X4A**.

## -returns

Type: **XMFLOAT3X4A &**

An lvalue reference to the current instance of **XMFLOAT3X4A**, after copying *arg1* into it.

## -see-also
[XMFLOAT3X4A structure](/windows/win32/api/directxmath/ns-directxmath-xmfloat3x4a)