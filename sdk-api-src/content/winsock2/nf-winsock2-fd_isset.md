---
UID: NF:winsock2.FD_ISSET
title: FD_ISSET macro (winsock2.h)
description: The FD_ISSET macro (winsock2.h) is used to check if a socket is included in a descriptor set
helpviewer_keywords: ["FD_ISSET","winsock/FD_ISSET"]
tech.root: WinSock
ms.date: 11/06/2023
ms.keywords: FD_ISSET, FD_ISSET macro [Winsock], winsock/FD_ISSET
req.header: winsock2.h
req.include-header: Winsock2.h, Winsock.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - FD_ISSET
 - winsock2/FD_ISSET
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
 - fd_isset
---

## -description

The **FD_ISSET** macro returns whether a socket is included in an [fd_set](/windows/win32/api/winsock2/ns-winsock2-fd_set) structure. A non-zero return value indicates that the socket is found in the set, otherwise the set does not contain the socket.

## -parameters

### -param fd

A descriptor identifying a socket which will be checked against the set.

### -param set

A pointer to an [fd_set](/windows/win32/api/winsock2/ns-winsock2-fd_set).

## -remarks

The **FD_ISSET** macro expands to a call of function [__WSAFDIsSet](/windows/win32/api/winsock2/nf-winsock2-__wsafdisset).

## -see-also

[WSAAsyncSelect](/windows/win32/api/winsock2/nf-winsock2-wsaasyncselect)

[WSAEventSelect](/windows/win32/api/winsock2/nf-winsock2-wsaeventselect")

[select](/windows/win32/api/winsock2/nf-winsock2-select")
