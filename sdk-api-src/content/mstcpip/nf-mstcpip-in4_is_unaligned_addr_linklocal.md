---
UID: NF:mstcpip.IN4_IS_UNALIGNED_ADDR_LINKLOCAL
tech.root: WinSock
title: IN4_IS_UNALIGNED_ADDR_LINKLOCAL
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
 - IN4_IS_UNALIGNED_ADDR_LINKLOCAL
f1_keywords:
 - IN4_IS_UNALIGNED_ADDR_LINKLOCAL
 - mstcpip/IN4_IS_UNALIGNED_ADDR_LINKLOCAL
dev_langs:
 - c++
helpviewer_keywords:
 - IN4_IS_UNALIGNED_ADDR_LINKLOCAL
---

## -description

Determines whether the address argument (which is permitted to be unaligned) is an IPv4 link-local address.

## -parameters

### -param a

Type: \_In\_ **CONST [IN_ADDR](/windows/win32/api/inaddr/ns-inaddr-in_addr) \***

Pointer (which is permitted to be unaligned) to the address to test.

## -returns

`true` if the address is an IPv4 link-local address; otherwise, `false`.

Returns `true` for local-use IPv4 unicast addresses. Returns `false` for the IPv4 loopback address. Doesn't return `true` for IPv4 multicast addresses of link-local scope.

## -remarks

## -see-also
