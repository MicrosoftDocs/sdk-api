---
UID: NF:directxmath.XMFLOAT3X4A.operator-assign
title: XMFLOAT3X4A::operator=
ms.date: 04/22/2020
description: Assigns the **XMFLOAT3X4A** argument's vector component data to the current instance of **XMFLOAT3X4A**.
tech.root: dxmath
f1_keywords:
- directxmath/XMFLOAT3X4A::operator=
dev_langs:
- c++
req.construct-type: function
req.header: directxmath.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace:
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
- apiref
- kbSyntax
api_type:
- COM
api_location:
- directxmath.h
api_name:
- XMFLOAT3X4A::operator=
targetos: Windows
req.typenames: 
req.redist: 
---

## -description

Assigns the **XMFLOAT3X4A** argument's vector component data to the current instance of **XMFLOAT3X4A**.

## -parameters

### -param arg1

Type: **const XMFLOAT3X4A &**

An lvalue reference to a constant **XMFLOAT3X4A** value whose vector component data the operator should copy into the current **XMFLOAT3X4A**.

## -returns

Type: **XMFLOAT3X4A &**

An lvalue reference to the current instance of **XMFLOAT3X4A**, after copying *arg1* into it.

## -see-also
[XMFLOAT3X4A structure](/windows/win32/api/directxmath/ns-directxmath-xmfloat3x4a)