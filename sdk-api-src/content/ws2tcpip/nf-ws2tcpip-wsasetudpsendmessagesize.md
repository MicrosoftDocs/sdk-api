---
UID: NF:ws2tcpip.WSASetUdpSendMessageSize
title: WSASetUdpSendMessageSize
author: windows-sdk-content
description: Sets the segmentation message size on a UDP socket.
tech.root: WinSock
ms.author: windowssdkdev
ms.date: 10/01/2019
ms.keywords: WSASetUdpSendMessageSize, WSASetUdpSendMessageSize function [Winsock], winsock.wsasetudpsendmessagesize, ws2tcpip/WSASetUdpSendMessageSize
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
 - WSASetUdpSendMessageSize
 - ws2tcpip/WSASetUdpSendMessageSize
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ws2_32.dll
api_name:
 - WSASetUdpSendMessageSize
---

## -description

Sets the segmentation message size on a UDP socket.

## -parameters

### -param Socket [in]

A descriptor that identifies a UDP socket.

### -param MsgSize [in]

Type: **[DWORD](/windows/win32/winprog/windows-data-types)**

The message size to be set on the socket for UDP segmentation.

## -returns

On success, the function returns 0. Otherwise, a value of [SOCKET_ERROR](/windows/win32/winsock/return-values-on-function-failure-2) is returned, and you can retrieve a specific error code by calling [WSAGetLastError](../winsock/nf-winsock-wsagetlasterror.md).

## -remarks

UDP send segmentation is supported through the [UDP_SEND_MSG_SIZE](/windows/win32/winsock/ipproto-udp-socket-options) socket option. **WSASetUdpSendMessageSize** is a type-safe wrapper for setting this socket option, and we recommend it over [setsockopt](../winsock/nf-winsock-setsockopt.md).

## -see-also