---
UID: NF:winsock2.FD_ZERO
title: FD_ZERO macro (winsock2.h)
description: The FD_ZERO macro (winsock2.h) is used to clear all sockets in a descriptor set
helpviewer_keywords: ["FD_ZERO","winsock/FD_ZERO"]
tech.root: WinSock
ms.date: 11/06/2023
ms.keywords: FD_ZERO, FD_ZERO macro [Winsock], winsock/FD_ZERO
req.header: winsock2.h
req.include-header: Winsock2.h, Winsock.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FD_ZERO
 - winsock/FD_ZERO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winsock.h
api_name:
 - fd_zero
---

## -description

The **FD_ZERO** macro clears all sockets in an [fd_set](/windows/win32/api/winsock2/ns-winsock2-fd_set) structure by setting the *fd_count* to 0.

## -parameters

### -param set

A pointer to an [fd_set](/windows/win32/api/winsock2/ns-winsock2-fd_set).

## -remarks

The **FD_ZERO** macro is used to clear an **fd_set** before any usage.

## -see-also

[WSAAsyncSelect](/windows/win32/api/winsock2/nf-winsock2-wsaasyncselect)

[WSAEventSelect](/windows/win32/api/winsock2/nf-winsock2-wsaeventselect)

[select](/windows/win32/api/winsock2/nf-winsock2-select)
