---
UID: NF:mstcpip.IN4_IS_ADDR_SITELOCAL
tech.root: WinSock
title: IN4_IS_ADDR_SITELOCAL
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
 - IN4_IS_ADDR_SITELOCAL
f1_keywords:
 - IN4_IS_ADDR_SITELOCAL
 - mstcpip/IN4_IS_ADDR_SITELOCAL
dev_langs:
 - c++
helpviewer_keywords:
 - IN4_IS_ADDR_SITELOCAL
---

## -description

Determines whether the address argument is an IPv4 site-local address.

## -parameters

### -param a

Type: \_In\_ **CONST [IN_ADDR](/windows/win32/api/inaddr/ns-inaddr-in_addr) \***

Pointer to the address to test.

## -returns

`true` if the address is an IPv4 site-local address; otherwise, `false`.

Returns `true` for local-use IPv4 unicast addresses.

## -remarks

## -see-also
