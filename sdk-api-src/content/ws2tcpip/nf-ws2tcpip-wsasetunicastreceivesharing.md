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

> [!IMPORTANT]
> Keep these caveats in mind when adopting the option:
>
> - Only endpoints that set the option to **TRUE** join the shared-delivery set. An endpoint at which the option is **FALSE** (the default) is never added and its receive behavior is unchanged.
> - The option affects unicast delivery only. Multicast and broadcast delivery are not changed.
> - The option is honored only by UDP sockets today (see the following note), so probe support per socket type rather than assuming availability.

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

### Port sharing and bindability

This option changes delivery only; it does not change the stack's bindability decisions. Whether multiple sockets are allowed to bind the same port is governed by the existing address-sharing options, and sharing a port with peer sockets typically requires [SO_REUSEADDR](/windows/win32/winsock/sol-socket-socket-options). There are narrower cases in which sockets can share a port without **SO_REUSEADDR**, but the scope of that implicit sharing is smaller and less general; applications that intend to share a port should set **SO_REUSEADDR** explicitly. For the rules that govern when multiple sockets may bind the same address and port, see [Using SO_REUSEADDR and SO_EXCLUSIVEADDRUSE](/windows/win32/winsock/using-so-reuseaddr-and-so-exclusiveaddruse).

## -examples

The following example opens a dual-stack UDP socket (an **AF_INET6** socket with **IPV6_V6ONLY** disabled, so it receives both IPv6 and IPv4 unicast traffic on the same port), confirms that shared unicast receive is supported before relying on it, opts in using the type-safe wrapper, binds the port, and then receives datagrams until the program is interrupted. Run several copies of the program on the same port to observe each instance receive a copy of every inbound unicast datagram.

```cpp
#include <winsock2.h>
#include <ws2tcpip.h>
#include <ws2ipdef.h>
#include <stdio.h>
#include <stdlib.h>

#pragma comment(lib, "ws2_32.lib")

#define DEFAULT_PORT 1234

//
// Create a dual-stack UDP socket: an AF_INET6 socket with IPV6_V6ONLY turned
// off accepts both IPv6 and IPv4 unicast datagrams on the same port (IPv4
// peers appear as IPv4-mapped IPv6 addresses). This lets a single socket serve
// both address families seamlessly.
//
static SOCKET
CreateDualStackUdpSocket(void)
{
    SOCKET s = socket(AF_INET6, SOCK_DGRAM, IPPROTO_UDP);
    DWORD v6Only;

    if (s == INVALID_SOCKET) {
        return INVALID_SOCKET;
    }

    v6Only = FALSE;
    if (setsockopt(s, IPPROTO_IPV6, IPV6_V6ONLY,
                   (const char*)&v6Only, sizeof(v6Only)) == SOCKET_ERROR) {
        closesocket(s);
        return INVALID_SOCKET;
    }

    return s;
}

//
// Probe whether SO_UNICAST_RECEIVE_SHARING is supported for the protocol this
// application uses. Support is per-socket-type, so probe a socket of the same
// type the application will actually use (here, dual-stack UDP). Probe each
// protocol separately rather than caching a single global answer.
//
// WSAGetUnicastReceiveSharing succeeds only when the option is supported, so
// it doubles as the feature-detection probe. A successful call means the
// feature is available; any failure (canonically WSAENOPROTOOPT) means it is
// not -- whether because of an older Windows version or an unsupported socket
// type. Do not branch on the specific error code.
//
static BOOL
IsUnicastReceiveSharingSupported(void)
{
    SOCKET probe = CreateDualStackUdpSocket();
    DWORD enabled;
    BOOL supported;

    if (probe == INVALID_SOCKET) {
        return FALSE;
    }

    supported = (WSAGetUnicastReceiveSharing(probe, &enabled) == 0);
    closesocket(probe);
    return supported;
}

int
__cdecl
main(
    _In_ int argc,
    _In_reads_(argc) char** argv
    )
{
    WSADATA wsaData;
    SOCKET s = INVALID_SOCKET;
    struct sockaddr_in6 addr = {0};
    DWORD optVal;
    USHORT port = DEFAULT_PORT;
    char buf[65536];
    int result;
    int exitCode = 1;

    if (argc > 1) {
        char* end;
        unsigned long parsedPort = strtoul(argv[1], &end, 10);
        if (argv[1][0] == '\0' || *end != '\0' ||
            parsedPort == 0 || parsedPort > 65535) {
            fprintf(stderr, "Invalid port: %s\n", argv[1]);
            return 1;
        }
        port = (USHORT)parsedPort;
    }

    result = WSAStartup(WINSOCK_VERSION, &wsaData);
    if (result != 0) {
        fprintf(stderr, "WSAStartup failed: %d\n", result);
        return 1;
    }

    //
    // Required: confirm the feature is available before relying on it. This
    // check is mandatory -- it covers both older Windows versions that do not
    // implement the option and socket types that do not support it.
    //
    if (!IsUnicastReceiveSharingSupported()) {
        fprintf(stderr,
                "SO_UNICAST_RECEIVE_SHARING is not supported on this "
                "machine/socket type; falling back to non-shared delivery.\n");
        //
        // Fall back to non-shared delivery here as appropriate for the
        // application. This sample simply exits.
        //
        goto Done;
    }

    s = CreateDualStackUdpSocket();
    if (s == INVALID_SOCKET) {
        fprintf(stderr, "failed to create dual-stack socket\n");
        goto Done;
    }

    //
    // SO_REUSEADDR typically allows several sockets to bind the same port so
    // they can share delivery. SO_UNICAST_RECEIVE_SHARING controls delivery
    // only; it does not change the stack's bindability decisions.
    //
    optVal = TRUE;
    if (setsockopt(s, SOL_SOCKET, SO_REUSEADDR,
                   (const char*)&optVal, sizeof(optVal)) == SOCKET_ERROR) {
        fprintf(stderr, "setsockopt(SO_REUSEADDR) failed: %d\n",
                WSAGetLastError());
        goto Done;
    }

    //
    // Opt in to shared unicast delivery using the type-safe wrapper (preferred
    // over calling setsockopt(SO_UNICAST_RECEIVE_SHARING) directly).
    //
    // This MUST be done before bind. Calling it on an already-bound socket
    // fails with WSAEINVAL and has no effect.
    //
    // SO_UNICAST_RECEIVE_SHARING is mutually exclusive with SO_EXCLUSIVEADDRUSE,
    // SO_REUSE_MULTICASTPORT, and the SIO_CPU_AFFINITY ioctl. Do not set any of
    // those on this socket; combining them causes this call (or the conflicting
    // call) to fail with WSAEOPNOTSUPP.
    //
    if (WSASetUnicastReceiveSharing(s, TRUE) == SOCKET_ERROR) {
        fprintf(stderr, "WSASetUnicastReceiveSharing() failed: %d\n",
                WSAGetLastError());
        goto Done;
    }

    //
    // Bind the wildcard IPv6 address (in6addr_any). Because the socket is
    // dual-stack, this single bind covers both IPv6 and IPv4 unicast traffic
    // for the chosen port.
    //
    addr.sin6_family = AF_INET6;
    addr.sin6_port = htons(port);
    addr.sin6_addr = in6addr_any;

    if (bind(s, (struct sockaddr*)&addr, sizeof(addr)) == SOCKET_ERROR) {
        fprintf(stderr, "bind() failed: %d\n", WSAGetLastError());
        goto Done;
    }

    printf("Listening on [::]:%u (IPv6 + IPv4, PID %lu) with shared unicast "
           "receive.\n", port, GetCurrentProcessId());
    printf("Launch additional instances of this program on the same port to\n"
           "observe each instance receive a copy of every inbound datagram.\n");
    printf("Press Ctrl+C to exit.\n\n");

    //
    // Receive until the program is interrupted. There is no in-band success
    // condition: the loop runs until the process is terminated, and the only
    // normal way to exit this sample is Ctrl+C. recv returns SOCKET_ERROR only
    // on an actual error, which breaks the loop below.
    //
    for (;;) {
        result = recv(s, buf, sizeof(buf), 0);
        if (result == SOCKET_ERROR) {
            fprintf(stderr, "recv() failed: %d\n", WSAGetLastError());
            break;
        }
        printf("recv: %d bytes\n", result);
    }


Done:
    if (s != INVALID_SOCKET) {
        closesocket(s);
    }
    WSACleanup();
    return exitCode;
}
```

## -see-also

* [WSAGetUnicastReceiveSharing](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsagetunicastreceivesharing)
* [SOL_SOCKET socket options](/windows/win32/winsock/sol-socket-socket-options)
* [Using SO_REUSEADDR and SO_EXCLUSIVEADDRUSE](/windows/win32/winsock/using-so-reuseaddr-and-so-exclusiveaddruse)
