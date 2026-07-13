---
UID: NF:winsock2.FD_SET
title: FD_SET macro (winsock2.h)
description: The FD_SET macro (winsock2.h) is used by Windows Sockets (Winsock) functions and service providers to place sockets into a set. 
helpviewer_keywords: ["FD_SET","_win32_fd_set_2","fd_set","fd_set structure [Winsock]","winsock.fd_set_2","winsock/fd_set"]
old-location: winsock\fd_set_2.htm
tech.root: WinSock
ms.assetid: 2af5d69d-190e-4814-8d8b-438431808625
ms.date: 08/03/2022
ms.keywords: FD_SET, _win32_fd_set_2, fd_set, fd_set structure [Winsock], winsock.fd_set_2, winsock/fd_set
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
 - FD_SET
 - winsock2/FD_SET
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
 - fd_set
---

## -description

The <b>FD_SET</b> macro adds a file descriptor to an <a href="/windows/win32/api/winsock2/ns-winsock2-fd_set">fd_set</a>. If the file descriptor already exist within the set, a duplicate will not be added.

## -parameters

### -param fd

A descriptor identifying a socket which will be added to the set.

### -param set

A pointer to a <b>fd_set</b>.

## -parameters

## -remarks

Be careful not to confuse the **FD_SET** macro with the typedef of the [fd_set](/windows/win32/api/winsock2/ns-winsock2-fd_set) structure that's also named **FD_SET**. That said, the **FD_SET** macro and the **fd_set** structure are related, and often used in conjunction.

## -see-also

<a href="/windows/win32/api/winsock/nf-winsock-wsaasyncselect">WSAAsyncSelect</a>



<a href="/windows/win32/api/winsock2/nf-winsock2-wsaeventselect">WSAEventSelect</a>



<a href="/windows/win32/api/winsock2/nf-winsock2-select">select</a>
