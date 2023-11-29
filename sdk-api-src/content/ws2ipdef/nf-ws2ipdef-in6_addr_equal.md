---
UID: NF:ws2ipdef.IN6_ADDR_EQUAL
tech.root: WinSock
title: IN6_ADDR_EQUAL
ms.date: 11/21/2023
targetos: Windows
description: 
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: ws2ipdef.h
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
 - ws2ipdef.h
api_name:
 - IN6_ADDR_EQUAL
f1_keywords:
 - IN6_ADDR_EQUAL
 - ws2ipdef/IN6_ADDR_EQUAL
dev_langs:
 - c++
helpviewer_keywords:
 - IN6_ADDR_EQUAL
---

## -description

Determines whether two IPv6 addresses are equal.

## -parameters

### -param x

Type: **CONST [IN6_ADDR](/windows/win32/api/in6addr/ns-in6addr-in6_addr) \***

Pointer to the first address.

### -param y

Type: **CONST [IN6_ADDR](/windows/win32/api/in6addr/ns-in6addr-in6_addr) \***

Pointer to the second address.

## -returns

`true` if the two addresses arguments point to values that are equal; otherwise, `false`.

## -remarks

## -see-also

