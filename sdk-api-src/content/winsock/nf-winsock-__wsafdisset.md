---
UID: NF:winsock.__WSAFDIsSet
title: __WSAFDIsSet function (winsock.h)
description: The __WSAFDIsSet function (winsock.h) specifies whether a socket is included in a set of socket descriptors.
helpviewer_keywords: ["__WSAFDIsSet","__WSAFDIsSet function [Winsock]","winsock.wsafdisset","winsock/__WSAFDIsSet"]
old-location: winsock\wsafdisset.htm
tech.root: WinSock
ms.assetid: ca420136-0b3b-45a1-85ce-83ab6ba1a70a
ms.date: 08/15/2022
ms.keywords: __WSAFDIsSet, __WSAFDIsSet function [Winsock], winsock.wsafdisset, winsock/__WSAFDIsSet
req.header: winsock.h
req.include-header: Winsock2.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1, Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ws2_32.lib
req.dll: Ws2_32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __WSAFDIsSet
 - winsock/__WSAFDIsSet
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ws2_32.dll
api_name:
 - __WSAFDIsSet
---

## -description

The **__WSAFDIsSet** function returns a value indicating whether a socket is included in a set of socket descriptors.

## -parameters

### -param unnamedParam1

A file descriptor identifying a socket.

### -param unnamedParam2

A pointer to an [fd_set](/windows/win32/api/winsock/ns-winsock-fd_set) structure containing the set of socket descriptors.

## -returns

A non-zero value if the socket specified in *unnamedParam1* is a member of the set specified in *unnamedParam2*; otherwise, 0.

## -remarks

**Windows Phone 8:** This function is supported for Windows Phone Store apps on Windows Phone 8 and later.

**Windows 8.1** and **Windows Server 2012 R2**: This function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and later.

The **FD_ISSET** macro expands to a call of function **__WSAFDIsSet**.

## -see-also

* [WSAAsyncSelect](/windows/win32/api/winsock/nf-winsock-wsaasyncselect)
* [WSAEventSelect](/windows/win32/api/winsock2/nf-winsock2-wsaeventselect)
* [fd_set](/windows/win32/api/winsock/ns-winsock-fd_set)
* [select](/windows/win32/api/winsock2/nf-winsock2-select)
