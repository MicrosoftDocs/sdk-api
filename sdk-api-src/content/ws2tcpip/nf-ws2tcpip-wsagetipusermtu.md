---
UID: NF:ws2tcpip.WSAGetIPUserMtu
title: WSAGetIPUserMtu
author: windows-sdk-content
description: Retrieves the user-defined IP layer MTU for a socket.
tech.root: WinSock
ms.author: windowssdkdev
ms.date: 10/02/2019
ms.keywords: WSAGetIPUserMtu, WSAGetIPUserMtu function [Winsock], winsock.wsagetipusermtu, ws2tcpip/WSAGetIPUserMtu
req.header: ws2tcpip.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 2004 (10.0; Build 19041)
req.target-min-winversvr: Windows Server, version 2004 (10.0; Build 19041)
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
f1_keywords:
 - WSAGetIPUserMtu
 - ws2tcpip/WSAGetIPUserMtu
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ws2_32.dll
api_name:
 - WSAGetIPUserMtu
---

## -description

Retrieves the user-defined IP layer MTU for a socket.

## -parameters

### -param Socket [in]

A descriptor that identifies a socket.

### -param Mtu [out]

Type: **[DWORD](/windows/win32/winprog/windows-data-types)\***

A pointer to a **DWORD**. On success, the function sets the DWORD to the user-defined IP layer MTU set on the socket.

## -returns

On success, the function returns 0. Otherwise, a value of [SOCKET_ERROR](/windows/win32/winsock/return-values-on-function-failure-2) is returned, and you can retrieve a specific error code by calling [WSAGetLastError](../winsock/nf-winsock-wsagetlasterror.md).

## -remarks

This functionality is supported through the [**IP_USER_MTU**](/windows/win32/winsock/ipproto-ip-socket-options) socket option. **WSAGetIPUserMtu** is a type-safe wrapper for getting this socket option, and we recommend it over [getsockopt](../winsock/nf-winsock-getsockopt.md).

## -see-also