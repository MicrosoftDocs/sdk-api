---
UID: NF:winsock2.FD_CLR
title: FD_CLR macro (winsock2.h)
description: The FD_CLR macro (winsock2.h) is used by Windows Sockets (Winsock) functions and service providers to remove sockets from a set.
tech.root: WinSock
ms.date: 11/06/2023
ms.keywords: FD_CLR, FD_CLR macro [Winsock]
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
 - FD_CLR
 - winsock2/FD_CLR
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
 - fd_clr
---

## -description

The **FD_CLR** macro removes a file descriptor from an [fd_set]("/windows/win32/api/winsock2/ns-winsock2-fd_set) structure. If there are multiple matches, only the first file descriptor will be removed.

## -parameters

### -param fd

A descriptor identifying a socket which will be removed from the set.

### -param set

A pointer to an [fd_set](/windows/win32/api/winsock2/ns-winsock2-fd_set).

## -see-also

[WSAAsyncSelect](/windows/win32/api/winsock2/nf-winsock2-wsaasyncselect)

[WSAEventSelect](/windows/win32/api/winsock2/nf-winsock2-wsaeventselect")

[select](/windows/win32/api/winsock2/nf-winsock2-select")
