---
UID: NF:ws2tcpip.WSASetIPUserMtu
title: WSASetIPUserMtu
author: windows-sdk-content
description: Sets the user-defined IP layer MTU on a socket.
tech.root: WinSock
ms.author: windowssdkdev
ms.date: 10/02/2019
ms.keywords: WSASetIPUserMtu, WSASetIPUserMtu function [Winsock], winsock.wsasetipusermtu, ws2tcpip/WSASetIPUserMtu
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
 - WSASetIPUserMtu
 - ws2tcpip/WSASetIPUserMtu
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ws2_32.dll
api_name:
 - WSASetIPUserMtu
---

## -description

Sets the user-defined IP layer MTU on a socket.

## -parameters

### -param Socket [in]

A descriptor that identifies a socket.

### -param Mtu [in]

Type: **[DWORD](/windows/win32/winprog/windows-data-types)**

The user-defined IP layer MTU to be set on the socket.

## -returns

On success, the function returns 0. Otherwise, a value of [SOCKET_ERROR](/windows/win32/winsock/return-values-on-function-failure-2) is returned, and you can retrieve a specific error code by calling [WSAGetLastError](../winsock/nf-winsock-wsagetlasterror.md).

## -remarks

This functionality is supported through the [**IP_USER_MTU**](/windows/win32/winsock/ipproto-ip-socket-options) socket option. **WSASetIPUserMtu** is a type-safe wrapper for setting this socket option, and we recommend it over [setsockopt](../winsock/nf-winsock-setsockopt.md).

## -see-also