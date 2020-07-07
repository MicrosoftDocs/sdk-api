---
UID: NF:ws2tcpip.WSAGetUdpSendMessageSize
title: WSAGetUdpSendMessageSize
author: windows-sdk-content
description: Retrieves the segmentation message size for a UDP socket.
tech.root: WinSock
ms.author: windowssdkdev
ms.date: 10/01/2019
ms.keywords: WSAGetUdpSendMessageSize, WSAGetUdpSendMessageSize function [Winsock], winsock.wsagetudpsendmessagesize, ws2tcpip/WSAGetUdpSendMessageSize
ms.topic: function
f1_keywords:
- ws2tcpip/WSAGetUdpSendMessageSize
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
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Ws2_32.dll
api_name:
- WSAGetUdpSendMessageSize
targetos: Windows
req.typenames: 
req.redist: 
---

## -description

Retrieves the segmentation message size for a UDP socket.

## -parameters

### -param Socket [in]

A descriptor that identifies a UDP socket.

### -param MsgSize [out]

Type: **[DWORD](/windows/win32/winprog/windows-data-types)\***

A pointer to a **DWORD**. On success, the function sets the DWORD to the message size used on the socket for UDP segmentation.

## -returns

On success, the function returns 0. Otherwise, a value of [SOCKET_ERROR](/windows/win32/winsock/return-values-on-function-failure-2) is returned, and you can retrieve a specific error code by calling [WSAGetLastError](/windows/win32/api/winsock/nf-winsock-wsagetlasterror).

## -remarks

UDP send segmentation is supported through the [UDP_SEND_MSG_SIZE](/windows/win32/winsock/ipproto-udp-socket-options) socket option. **WSAGetUdpSendMessageSize** is a type-safe wrapper for getting this socket option, and we recommend it over [getsockopt](/windows/win32/api/winsock/nf-winsock-getsockopt).

## -see-also
