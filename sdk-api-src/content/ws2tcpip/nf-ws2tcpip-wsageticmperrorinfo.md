---
UID: NF:ws2tcpip.WSAGetIcmpErrorInfo
title: WSAGetIcmpErrorInfo
author: windows-sdk-content
description: Retrieves information about an ICMP error received on a TCP socket during connection setup.
tech.root: WinSock
ms.author: windowssdkdev
ms.date: 10/02/2019
ms.keywords: WSAGetIcmpErrorInfo, WSAGetIcmpErrorInfo function [Winsock], winsock.wsageticmperrorinfo, ws2tcpip/WSAGetIcmpErrorInfo
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
 - WSAGetIcmpErrorInfo
 - ws2tcpip/WSAGetIcmpErrorInfo
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ws2_32.dll
api_name:
 - WSAGetIcmpErrorInfo
---

## -description

Retrieves information about an ICMP error received on a TCP socket during connection setup.

## -parameters

### -param Socket [in]

A descriptor that identifies a TCP socket.

### -param Info [out]

Type: **[DWORD](/windows/win32/winprog/windows-data-types)\***

A pointer to an [ICMP_ERROR_INFO](../ws2ipdef/ns-ws2ipdef-icmp_error_info.md) structure. On success, the function initializes the structure.

## -returns

On success, the function returns 0. Otherwise, a value of [SOCKET_ERROR](/windows/win32/winsock/return-values-on-function-failure-2) is returned, and you can retrieve a specific error code by calling [WSAGetLastError](../winsock/nf-winsock-wsagetlasterror.md).

## -remarks

If no ICMP error has been received since the last connect call, then [**WSANO_DATA**](/windows/win32/winsock/windows-sockets-error-codes-2) is returned. This functionality is supported through the [**TCP_ICMP_ERROR_INFO**](/windows/win32/winsock/ipproto-tcp-socket-options) socket option. **WSAGetIcmpErrorInfo** is a type-safe wrapper for getting this socket option, and we recommend it over [getsockopt](../winsock/nf-winsock-getsockopt.md).

## -see-also