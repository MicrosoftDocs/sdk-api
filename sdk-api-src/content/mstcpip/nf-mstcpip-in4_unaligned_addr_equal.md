---
UID: NF:mstcpip.IN4_UNALIGNED_ADDR_EQUAL
tech.root: WinSock
title: IN4_UNALIGNED_ADDR_EQUAL
ms.date: 11/21/2023
targetos: Windows
description: 
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: mstcpip.h
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
 - mstcpip.h
api_name:
 - IN4_UNALIGNED_ADDR_EQUAL
f1_keywords:
 - IN4_UNALIGNED_ADDR_EQUAL
 - mstcpip/IN4_UNALIGNED_ADDR_EQUAL
dev_langs:
 - c++
helpviewer_keywords:
 - IN4_UNALIGNED_ADDR_EQUAL
---

## -description

Determines whether two IPv4 addresses are equal (where the pointer arguments are permitted to be unaligned).

## -parameters

### -param a

Type: \_In\_ **CONST [IN_ADDR](/windows/win32/api/inaddr/ns-inaddr-in_addr) \***

Pointer (which is permitted to be unaligned) to the first address.

### -param b

Type: \_In\_ **CONST [IN_ADDR](/windows/win32/api/inaddr/ns-inaddr-in_addr) \***

Pointer (which is permitted to be unaligned) to the second address.

## -returns

`true` if the two addresses arguments point to values that are equal; otherwise, `false`.

## -remarks

## -see-also
