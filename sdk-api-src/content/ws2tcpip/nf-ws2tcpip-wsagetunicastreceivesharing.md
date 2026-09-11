---
UID: NF:ws2tcpip.WSAGetUnicastReceiveSharing
title: WSAGetUnicastReceiveSharing
description: Retrieves whether a datagram socket has opted in to shared delivery of inbound unicast datagrams via the SO_UNICAST_RECEIVE_SHARING socket option.
tech.root: WinSock
ms.date: 05/15/2026
req.header: ws2tcpip.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 11
req.target-min-winversvr: Windows Server 2025
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
 - WSAGetUnicastReceiveSharing
 - ws2tcpip/WSAGetUnicastReceiveSharing
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ws2tcpip.h
api_name:
 - WSAGetUnicastReceiveSharing
---

## -description

Retrieves whether a datagram socket has opted in to shared delivery of inbound unicast datagrams via the [SO_UNICAST_RECEIVE_SHARING](/windows/win32/winsock/sol-socket-socket-options) socket option.

> [!NOTE]
> The option is defined at **SOL_SOCKET** scope and is conceptually protocol-agnostic, but it is currently honored only by UDP sockets. To determine whether a given socket supports shared unicast delivery, call **WSAGetUnicastReceiveSharing** on it: a successful return means shared delivery is supported on that socket; any failure means it is not. See [Detecting feature support at runtime](#detecting-feature-support-at-runtime) in *Remarks*.

## -parameters

### -param Socket [in]

A descriptor that identifies a datagram socket.

### -param Enabled [out]

Type: **[DWORD](/windows/win32/winprog/windows-data-types)\***

A pointer to a **DWORD**. On success, set to **TRUE** if the socket is opted in to shared unicast delivery, or **FALSE** otherwise.

## -returns

If the function succeeds, the return value is 0. Otherwise, a value of [SOCKET_ERROR](/windows/win32/winsock/return-values-on-function-failure-2) is returned, and you can retrieve a specific error code by calling [WSAGetLastError](../winsock/nf-winsock-wsagetlasterror.md). The expected failure code on Windows versions that do not implement this option is **WSAENOPROTOOPT**.

## -remarks

Shared unicast delivery is configured through the [SO_UNICAST_RECEIVE_SHARING](/windows/win32/winsock/sol-socket-socket-options) socket option. **WSAGetUnicastReceiveSharing** is a type-safe wrapper for reading this option and is recommended over calling [getsockopt](../winsock/nf-winsock-getsockopt.md) directly.

### Detecting feature support at runtime

**WSAGetUnicastReceiveSharing** doubles as the supported-by-this-socket probe. Open a socket of the protocol the application intends to use (typically UDP) and call this function on it:

* If the call returns 0, shared unicast delivery is supported for that socket; the application may safely call [WSASetUnicastReceiveSharing](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsasetunicastreceivesharing) on similarly-created sockets before binding them.
* If the call returns **SOCKET_ERROR**, shared unicast delivery is *not* supported for that socket on this machine, and the application should fall back to non-shared delivery. This single check covers both "the running version of Windows does not implement the option" and "this socket type is not supported"; applications do not need to distinguish the two. The canonical failure code is **WSAENOPROTOOPT** (10042), but applications should not branch on a specific error code.

Because support is determined per-socket-type, an application that uses multiple protocols should probe each protocol separately rather than caching a single global answer.

For a complete worked example that probes for support with **WSAGetUnicastReceiveSharing** and then opts in with [WSASetUnicastReceiveSharing](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsasetunicastreceivesharing), see the Examples section of [WSASetUnicastReceiveSharing](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsasetunicastreceivesharing).

## -see-also

* [WSASetUnicastReceiveSharing](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsasetunicastreceivesharing)
* [SOL_SOCKET socket options](/windows/win32/winsock/sol-socket-socket-options)
