---
UID: NS:winsock2.fd_set
title: fd_set (winsock2.h)
description: Fd_set structure is used by Windows Sockets (Winsock) functions and service providers to place sockets into a set. (fd_set)
helpviewer_keywords: ["*LPFD_SET","*PFD_SET","FD_SET","_win32_fd_set_2","fd_set","fd_set structure [Winsock]","winsock.fd_set_2","winsock/fd_set"]
old-location: winsock\fd_set_2.htm
tech.root: WinSock
ms.assetid: 2af5d69d-190e-4814-8d8b-438431808625
ms.date: 12/05/2018
ms.keywords: '*LPFD_SET, *PFD_SET, FD_SET, _win32_fd_set_2, fd_set, fd_set structure [Winsock], winsock.fd_set_2, winsock/fd_set'
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
req.typenames: fd_set, FD_SET, *PFD_SET, *LPFD_SET
req.redist: 
ms.custom: 19H1
f1_keywords:
 - fd_set
 - winsock2/fd_set
 - PFD_SET
 - winsock2/PFD_SET
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

# fd_set structure


## -description

The 
<b>fd_set</b> structure is used by various Windows Sockets functions and service providers, such as the 
<a href="/windows/desktop/api/winsock2/nf-winsock2-select">select</a> function, to place sockets into a "set" for various purposes, such as testing a given socket for readability using the <i>readfds</i> parameter of the 
<b>select</b> function.

## -struct-fields

### -field fd_count

The number of sockets in the set.

### -field fd_array

An array of sockets that are in the set.

## -see-also

<a href="/windows/desktop/api/winsock/nf-winsock-wsaasyncselect">WSAAsyncSelect</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaeventselect">WSAEventSelect</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-select">select</a>
