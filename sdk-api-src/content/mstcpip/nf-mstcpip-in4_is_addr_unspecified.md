---
UID: NF:mstcpip.IN4_IS_ADDR_UNSPECIFIED
tech.root: WinSock
title: IN4_IS_ADDR_UNSPECIFIED
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
 - IN4_IS_ADDR_UNSPECIFIED
f1_keywords:
 - IN4_IS_ADDR_UNSPECIFIED
 - mstcpip/IN4_IS_ADDR_UNSPECIFIED
dev_langs:
 - c++
helpviewer_keywords:
 - IN4_IS_ADDR_UNSPECIFIED
---

## -description

Determines whether the address argument is the unspecified IPv4 address (inaddr_any).

## -parameters

### -param a

Type: \_In\_ **CONST [IN_ADDR](/windows/win32/api/inaddr/ns-inaddr-in_addr) \***

Pointer to the address to test.

## -returns

`true` if the address is the unspecified IPv4 address (inaddr_any); otherwise, `false`.

## -remarks

## -see-also
