---
UID: NF:ws2tcpip.WSASetUnicastReceiveSharing
title: WSASetUnicastReceiveSharing
description: Opts a datagram socket in to (or out of) shared delivery of inbound unicast datagrams via the SO_UNICAST_RECEIVE_SHARING socket option.
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
 - WSASetUnicastReceiveSharing
 - ws2tcpip/WSASetUnicastReceiveSharing
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ws2tcpip.h
api_name:
 - WSASetUnicastReceiveSharing
---

## -description

Opts a datagram socket in to (or out of) shared delivery of inbound unicast datagrams via the [SO_UNICAST_RECEIVE_SHARING](/windows/win32/winsock/sol-socket-socket-options) socket option.

When this option is **TRUE** on a datagram socket at bind time, each inbound unicast datagram destined for the bound port is indicated both to the single endpoint that would have received it in the absence of this option *and* to every other endpoint on the same port at which the option is also **TRUE**. Endpoints at which the option is **FALSE** (the default) are not added to the shared-delivery set; their receive behavior is unchanged from previous releases.

The option only affects delivery of unicast datagrams. Multicast and broadcast delivery are unchanged.

> [!NOTE]
> The option is defined at **SOL_SOCKET** scope and is conceptually protocol-agnostic, but it is currently honored only by UDP sockets. To determine whether a given socket supports shared unicast delivery, call [WSAGetUnicastReceiveSharing](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsagetunicastreceivesharing) on it before binding: a successful return means shared delivery is supported on that socket; any failure means it is not. See [Detecting feature support at runtime](#detecting-feature-support-at-runtime) in *Remarks*.

The option must be set before the socket is bound; setting it on an already-bound socket fails. It is mutually exclusive with the **SO_EXCLUSIVEADDRUSE** and **SO_REUSE_MULTICASTPORT** socket options and with the **SIO_CPU_AFFINITY** ioctl; setting any of those after enabling shared delivery, or enabling shared delivery after setting any of those, fails. Sharing a port with peer sockets typically also requires [SO_REUSEADDR](/windows/win32/winsock/sol-socket-socket-options).

## -parameters

### -param Socket [in]

A descriptor that identifies a datagram socket. The option must be set before the socket is bound.

### -param Enabled [in]

Type: **[DWORD](/windows/win32/winprog/windows-data-types)**

**TRUE** to opt in to shared unicast receive delivery; **FALSE** to opt out (default).

## -returns

If the function succeeds, the return value is 0. Otherwise, a value of [SOCKET_ERROR](/windows/win32/winsock/return-values-on-function-failure-2) is returned, and you can retrieve a specific error code by calling [WSAGetLastError](../winsock/nf-winsock-wsagetlasterror.md). Notable failure codes include:

* **WSAEINVAL** — the socket has already been bound.
* **WSAEOPNOTSUPP** — the socket has a conflicting option set (for example, **SO_EXCLUSIVEADDRUSE**, **SO_REUSE_MULTICASTPORT**, or the **SIO_CPU_AFFINITY** ioctl).
* **WSAENOPROTOOPT** — the option is not implemented on the running version of Windows.

Applications should not depend on these exact codes for branching logic beyond runtime feature detection (see *Remarks*).

## -remarks

Shared unicast delivery is configured through the [SO_UNICAST_RECEIVE_SHARING](/windows/win32/winsock/sol-socket-socket-options) socket option. **WSASetUnicastReceiveSharing** is a type-safe wrapper for setting this option and is recommended over calling [setsockopt](../winsock/nf-winsock-setsockopt.md) directly.

### Detecting feature support at runtime

Use [WSAGetUnicastReceiveSharing](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsagetunicastreceivesharing) as the supported-by-this-socket probe. Open a socket of the protocol the application intends to use (typically UDP) and call that function on it before binding:

* If the call returns 0, shared unicast delivery is supported for that socket; **WSASetUnicastReceiveSharing** may then be called on similarly-created sockets before binding them.
* If the call returns **SOCKET_ERROR**, shared unicast delivery is *not* supported for that socket on this machine, and the application should fall back to non-shared delivery. This single check covers both "the running version of Windows does not implement the option" and "this socket type is not supported"; applications do not need to distinguish the two. The canonical failure code is **WSAENOPROTOOPT** (10042), but applications should not branch on a specific error code.

Because support is determined per-socket-type, an application that uses multiple protocols should probe each protocol separately rather than caching a single global answer.

## -see-also

* [WSAGetUnicastReceiveSharing](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsagetunicastreceivesharing)
* [SOL_SOCKET socket options](/windows/win32/winsock/sol-socket-socket-options)
