---
UID: NF:ws2tcpip.WSAGetUdpRecvMaxCoalescedSize
title: WSAGetUdpRecvMaxCoalescedSize
author: windows-sdk-content
description: Retrieves the maximum size of a received, coalesced message for a UDP socket.
tech.root: WinSock
ms.author: windowssdkdev
ms.date: 10/01/2019
ms.keywords: WSAGetUdpRecvMaxCoalescedSize, WSAGetUdpRecvMaxCoalescedSize function [Winsock], winsock.wsagetudprecvmaxcoalescedsize, ws2tcpip/WSAGetUdpRecvMaxCoalescedSize
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
 - WSAGetUdpRecvMaxCoalescedSize
 - ws2tcpip/WSAGetUdpRecvMaxCoalescedSize
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ws2_32.dll
api_name:
 - WSAGetUdpRecvMaxCoalescedSize
---

## -description

Retrieves the maximum size of a received, coalesced message for a UDP socket.

## -parameters

### -param Socket [in]

A descriptor that identifies a UDP socket.

### -param MaxCoalescedMsgSize [out]

Type: **[DWORD](/windows/win32/winprog/windows-data-types)\***

A pointer to a **DWORD**. On success, the function sets the DWORD to the maximum coalesced message size used on the socket for UDP receive coalescing.

## -returns

On success, the function returns 0. Otherwise, a value of [SOCKET_ERROR](/windows/win32/winsock/return-values-on-function-failure-2) is returned, and you can retrieve a specific error code by calling [WSAGetLastError](../winsock/nf-winsock-wsagetlasterror.md).

## -remarks

UDP receive coalescing is supported through the [UDP_RECV_MAX_COALESCED_SIZE](/windows/win32/winsock/ipproto-udp-socket-options) socket option. **WSAGetUdpRecvMaxCoalescedSize** is a type-safe wrapper for getting this socket option, and we recommend it over [getsockopt](../winsock/nf-winsock-getsockopt.md).

## -see-also