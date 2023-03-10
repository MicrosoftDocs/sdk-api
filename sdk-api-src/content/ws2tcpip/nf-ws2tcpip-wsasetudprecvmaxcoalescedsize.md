---
UID: NF:ws2tcpip.WSASetUdpRecvMaxCoalescedSize
title: WSASetUdpRecvMaxCoalescedSize
author: windows-sdk-content
description: Sets the maximum size of a coalesced message set on a UDP socket.
tech.root: WinSock
ms.author: windowssdkdev
ms.date: 10/01/2019
ms.keywords: WSASetUdpRecvMaxCoalescedSize, WSASetUdpRecvMaxCoalescedSize function [Winsock], winsock.wsasetudprecvmaxcoalescedsize, ws2tcpip/WSASetUdpRecvMaxCoalescedSize
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
 - WSASetUdpRecvMaxCoalescedSize
 - ws2tcpip/WSASetUdpRecvMaxCoalescedSize
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ws2_32.dll
api_name:
 - WSASetUdpRecvMaxCoalescedSize
---

## -description

Sets the maximum size of a coalesced message set on a UDP socket.

## -parameters

### -param Socket [in]

A descriptor that identifies a UDP socket.

### -param MaxCoalescedMsgSize [in]

Type: **[DWORD](/windows/win32/winprog/windows-data-types)**

The maximum coalesced message size to be set on the socket for UDP receive coalescing.

## -returns

On success, the function returns 0. Otherwise, a value of [SOCKET_ERROR](/windows/win32/winsock/return-values-on-function-failure-2) is returned, and you can retrieve a specific error code by calling [WSAGetLastError](../winsock/nf-winsock-wsagetlasterror.md).

## -remarks

UDP receive coalescing is supported through the [UDP_RECV_MAX_COALESCED_SIZE](/windows/win32/winsock/ipproto-udp-socket-options) socket option. **WSASetUdpRecvMaxCoalescedSize** is a type-safe wrapper for setting this socket option, and we recommend it over [setsockopt](../winsock/nf-winsock-setsockopt.md).

## -see-also