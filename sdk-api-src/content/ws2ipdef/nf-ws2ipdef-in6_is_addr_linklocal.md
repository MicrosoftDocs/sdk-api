---
UID: NF:ws2ipdef.IN6_IS_ADDR_LINKLOCAL
tech.root: WinSock
title: IN6_IS_ADDR_LINKLOCAL
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
 - IN6_IS_ADDR_LINKLOCAL
f1_keywords:
 - IN6_IS_ADDR_LINKLOCAL
 - ws2ipdef/IN6_IS_ADDR_LINKLOCAL
dev_langs:
 - c++
helpviewer_keywords:
 - IN6_IS_ADDR_LINKLOCAL
---

## -description

Determines whether the address argument is an IPv6 link-local address.

## -parameters

### -param a

Type: **CONST [IN6_ADDR](/windows/win32/api/in6addr/ns-in6addr-in6_addr) \***

Pointer to the address to test.

## -returns

`true` if the address is an IPv6 link-local address; otherwise, `false`.

Returns `true` for local-use IPv6 unicast addresses. Returns `false` for the IPv6 loopback address. Doesn't return `true` for IPv6 multicast addresses of link-local scope.

## -remarks

## -see-also
