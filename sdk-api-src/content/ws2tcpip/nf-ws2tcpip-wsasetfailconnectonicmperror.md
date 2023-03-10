---
UID: NF:ws2tcpip.WSASetFailConnectOnIcmpError
title: WSASetFailConnectOnIcmpError
author: windows-sdk-content
description: Sets the state of the [**TCP_FAIL_CONNECT_ON_ICMP_ERROR**](/windows/win32/winsock/ipproto-tcp-socket-options) socket option.
tech.root: WinSock
ms.author: windowssdkdev
ms.date: 10/02/2019
ms.keywords: WSASetFailConnectOnIcmpError, WSASetFailConnectOnIcmpError function [Winsock], winsock.wsasetfailconnectonicmperror, ws2tcpip/WSASetFailConnectOnIcmpError
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
 - WSASetFailConnectOnIcmpError
 - ws2tcpip/WSASetFailConnectOnIcmpError
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ws2_32.dll
api_name:
 - WSASetFailConnectOnIcmpError
---

## -description

Sets the state of the [**TCP_FAIL_CONNECT_ON_ICMP_ERROR**](/windows/win32/winsock/ipproto-tcp-socket-options) socket option.

## -parameters

### -param Socket [in]

A descriptor that identifies a TCP socket.

### -param Enabled [in]

Type: **[DWORD](/windows/win32/winprog/windows-data-types)**

A non-zero value if [**TCP_FAIL_CONNECT_ON_ICMP_ERROR**](/windows/win32/winsock/ipproto-tcp-socket-options) should be enabled, otherwise zero.

## -returns

On success, the function returns 0. Otherwise, a value of [SOCKET_ERROR](/windows/win32/winsock/return-values-on-function-failure-2) is returned, and you can retrieve a specific error code by calling [WSAGetLastError](../winsock/nf-winsock-wsagetlasterror.md).

## -remarks

This functionality is supported through the [**TCP_FAIL_CONNECT_ON_ICMP_ERROR**](/windows/win32/winsock/ipproto-tcp-socket-options) socket option. **WSASetFailConnectOnIcmpError** is a type-safe wrapper for setting this socket option, and we recommend it over [setsockopt](../winsock/nf-winsock-setsockopt.md).

## -see-also