---
UID: NC:ws2spi.LPWSPSETSOCKOPT
title: LPWSPSETSOCKOPT
description: The LPWSPSetSockOpt function sets a socket option.
tech.root: winsock
helpviewer_keywords: ["LPWSPSETSOCKOPT"]
ms.date: 9/12/2019
ms.keywords: LPWSPSETSOCKOPT
targetos: Windows
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: ws2spi.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - LibDef
api_location:
 - ws2spi.h
api_name:
 - LPWSPSETSOCKOPT
f1_keywords:
 - LPWSPSETSOCKOPT
 - ws2spi/LPWSPSETSOCKOPT
---

## -description

The **LPWSPSetSockOpt** function sets a socket option.

## -parameters

### -param s [in]

The descriptor that identifies a socket.

### -param level [in]

The level at which the option is defined; the supported levels include <b><a href="/windows/win32/winsock/sol-socket-socket-options">SOL_SOCKET</a></b>. For more information, see [Winsock Annexes](/windows/win32/winsock/winsock-annexes).

### -param optname [in]

The socket option for which the value is to be set.

### -param optval [in]

A pointer to the buffer in which the value for the requested option is supplied.

### -param optlen [in]

The size, in bytes, of the <i>optval</i> buffer.

### -param lpErrno [out]

A pointer to the error code.

## -returns

If no error occurs, **LPWSPSetSockOpt** returns zero. Otherwise, a value of **SOCKET_ERROR** is returned, and a specific error code is available in <i>lpErrno</i>.

<table>
<tr>
<th>Error Code</th>
<th>Meaning</th>
</tr>

<tr>
<td width="40%">
<dl>                                              
<dt><a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAENETDOWN">WSAENETDOWN</a></dt>
</dl>
</td>
<td width="60%">
The network subsystem has failed.
</td>
</tr>

<tr>
<td width="40%">
<dl>                                              
<dt><a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAEFAULT">WSAEFAULT</a></dt>
</dl>
</td>
<td width="60%">
The <i>optval</i> is not in a valid part of the process address space or <i>optlen</i> parameter is too small.
</td>
</tr>

<tr>
<td width="40%">
<dl>                                              
<dt><a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAEINPROGRESS">WSAEINPROGRESS</a></dt>
</dl>
</td>
<td width="60%">
Function is invoked when a callback is in progress.
</td>
</tr>

<tr>
<td width="40%">
<dl>                                              
<dt><a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAEINPROGRESS">WSAEINPROGRESS</a></dt>
</dl>
</td>
<td width="60%">
Blocking Windows Sockets call is in progress, or the service provider is still processing a callback function.
</td>
</tr>

<tr>
<td width="40%">
<dl>                                              
<dt><a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAEINVAL">WSAEINVAL</a></dt>
</dl>
</td>
<td width="60%">
The <i>level</i> is not valid, or the information in <i>optval</i> is not valid.
</td>
</tr>

<tr>
<td width="40%">
<dl>                                              
<dt><a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAENETRESET">WSAENETRESET</a></dt>
</dl>
</td>
<td width="60%">
The connection has been broken due to keep-alive activity detecting a failure while the operation was in progress.
</td>
</tr>

<tr>
<td width="40%">
<dl>                                              
<dt><b><a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAENOPROTOOPT">WSAENOPROTOOPT</a></b></dl>
</dl>
</td>
<td width="60%">
Option is unknown or unsupported for the specified provider.
</td>
</tr>

<tr>
<td width="40%">
<dl>                                              
<dt><b><a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAENOTCONN">WSAENOTCONN</a></b></dl>
</dl>
</td>
<td width="60%">
The connection has been reset when <a href="/windows/win32/winsock/so-keepalive">SO_KEEPALIVE</a> is set.
</td>
</tr>
<tr>
<td width="40%">
<dl>                                              
<dt><b><a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAENOTSOCK">WSAENOTSOCK</a></b></dl>
</dl>
</td>
<td width="60%">
The descriptor is not a socket.
</td>
</tr>
</table>

## -remarks

The **LPWSPSetSockOpt** function sets the current value for a socket option associated with a socket of any type, in any state. Although options can exist at multiple protocol levels, they are always present at the uppermost socket level. Options affect socket operations, such as whether broadcast messages can be sent on the socket.

There are two types of socket options: Boolean options that enable or disable a feature or behavior, and options that require an integer value or structure. To enable a Boolean option, <i>optval</i> points to a nonzero integer. To disable the option, <i>optval</i> points to an integer equal to zero. The <i>optlen</i> parameter should be equal to sizeof (int) for Boolean options. For other options, <i>optval</i> points to an integer or structure that contains the desired value for the option, and <i>optlen</i> is the length of the integer or structure.

For more information about socket options, see <b><a href="/windows/win32/winsock/socket-options">Socket Options</a></b>.

### level = SOL_SOCKET



| Value                                 | Type                       | Meaning                                                                                                                                                                                                                                                                                         |
|---------------------------------------|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SO_BROADCAST                         | BOOL                       | Enables transmission and receipt of broadcast messages on the socket.                                                                                                                                                                                                                           |
| SO_DEBUG                             | BOOL                       | Records debugging information.                                                                                                                                                                                                                                                                  |
| SO_DONTLINGER                        | BOOL                       | Reserved.                                                                                                                                                                                                                                                                                       |
| SO_DONTROUTE                         | BOOL                       | Disabled routing: send directly to an interface. Setting this socket option succeeds but is ignored on AF_INET sockets; fails on AF_INET6 sockets with <a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAENOPROTOOPT">WSAENOPROTOOPT</a> . This option is not supported on ATM sockets (results in an error). |
| SO_GROUP_PRIORITY                   | int                        | Reserved.                                                                                                                                                                                                                                                                                       |
| <b><a href="/windows/win32/winsock/so-keepalive">SO_KEEPALIVE</a></b> | BOOL                       | Sends keep-alives. Not supported on ATM sockets (results in an error).                                                                                                                                                                                                                          |
| SO_LINGER                            | struct linger              | Lingers on close if unsent data is present.                                                                                                                                                                                                                                                     |
| SO_OOBINLINE                         | BOOL                       | Receives OOB data in the normal data stream.                                                                                                                                                                                                                                                    |
| SO_RCVBUF                            | int                        | Specifies the total per-socket buffer space reserved for receives. This is unrelated to SO_MAX_MSG_SIZE and does not necessarily correspond to the size of the TCP receive window.                                                                                                           |
| SO_REUSEADDR                         | BOOL                       | Allows the socket to be bound to an address that is already in use. (See <b><a href="/windows/win32/api/winsock/nf-winsock-bind">Bind</a></b>.) Not applicable on ATM sockets.                                                                                                                                                                |
| SO_SNDBUF                            | int                        | Specifies the total per-socket buffer space reserved for sends. This is unrelated to SO_MAX_MSG_SIZE and does not necessarily correspond to the size of a TCP send window.                                                                                                                   |
| PVD_CONFIG                           | Service Provider Dependent | This object stores the configuration information for the service provider associated with socket <i>s</i>. The exact format of this data structure is service provider specific.                                                                                                                     |



 

Calling <b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspgetsockopt">LPWSPGetSockopt</a></b> with an unsupported option will result in an error code of <a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAENOPROTOOPT">WSAENOPROTOOPT</a>  returned in <i>lpErrno</i>.

<dl> <dt>

<span id="SO_DEBUG"></span><span id="so_debug"></span>SO_DEBUG
</dt> <dd>

Windows Sockets service providers are encouraged, but not required, to supply output debug information if the **SO_DEBUG** option is set by a Windows Sockets SPI client. The mechanism for generating the debug information and the format are beyond the scope of this specification.

</dd> <dt>

<span id="SO_GROUP_PRIORITY"></span><span id="so_group_priority"></span>SO_GROUP_PRIORITY
</dt> <dd>

Reserved.

</dd> <dt>

<span id="SO_KEEPALIVE"></span><span id="so_keepalive"></span><b><a href="/windows/win32/winsock/so-keepalive">SO_KEEPALIVE</a></b>
</dt> <dd>

A Windows Sockets SPI client can request that a TCP/IP provider enable the use of keep-alive packets on TCP connections by turning on the <b><a href="/windows/win32/winsock/so-keepalive">SO_KEEPALIVE</a></b> socket option. A Windows Sockets provider need not support the use of keep-alives: if it does, the precise semantics are implementation specific, but should conform to section 4.2.3.6 of RFC 1122: <i>Requirements for Internet Hosts—Communication Layers</i>. (This resource may only be available in English.) If a connection is dropped as the result of keep-alive the error code <a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAENETRESET">WSAENETRESET</a>  is returned to any calls in progress on the socket, and any subsequent calls will fail with <a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAENOTCONN">WSAENOTCONN</a> .

</dd> <dt>

<span id="SO_LINGER"></span><span id="so_linger"></span>SO_LINGER
</dt> <dd>

SO_LINGER controls the action taken when unsent data is queued on a socket and a <b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspclosesocket">LPWSPCloseSocket</a></b> is performed. See **LPWSPCloseSocket** for a description of the way in which the **SO_LINGER** settings affect the semantics of **LPWSPCloseSocket**. The Windows Sockets SPI client sets the desired behavior by creating a <b><a href="/windows/win32/api/winsock2/ns-winsock2-linger">LINGER</a></b> structure, pointed to by the <i>optval</i> parameter, with the following elements.

```cpp
struct linger {
  u_short l_onoff;
  u_short l_linger;
}
```

To enable **SO_LINGER**, a Windows Sockets SPI client should set **l_onoff** to a nonzero value, set **l_linger** to zero or the desired time-out, in seconds, and call **LPWSPSetSockOpt**. To enable **SO_DONTLINGER**, that is, disable SO_LINGER, **l_onoff** should be set to zero and **LPWSPSetSockOpt** should be called. Be aware that enabling **SO_LINGER** with a nonzero time-out on a nonblocking socket is not recommended. For more information, see <b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspclosesocket">LPWSPCloseSocket</a></b>.

Enabling **SO_LINGER** also disables **SO_DONTLINGER**, and vice versa. Be aware that if **SO_DONTLINGER** is disabled (that is, **SO_LINGER** is enabled) then no time-out value is specified. In this case, the time-out used is implementation dependent. If a previous time-out has been established for a socket (by enabling **SO_LINGER**), then this time-out value should be reinstated by the service provider.

</dd> <dt>

<span id="SO_REUSEADDR"></span><span id="so_reuseaddr"></span>SO_REUSEADDR
</dt> <dd>

By default, a socket cannot be bound (for more information, see <b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspbind">LPWSPBind</a></b>) to a local address that is already in use. On occasion, however, it may be desirable to reuse an address in this way. Because every connection is uniquely identified by the combination of local and remote addresses, there is no problem with having two sockets bound to the same local address as long as the remote addresses are different. To inform the Windows Sockets provider that a **LPWSPBind** on a socket should be allowed to bind to a local address that is already in use by another socket, the Windows Sockets SPI client should set the **SO_REUSEADDR** socket option for the socket before issuing the **LPWSPBind**. Be aware that the option is interpreted only at the time of the **LPWSPBind**: it is therefore unnecessary, but harmless, to set the option on a socket that is not to be bound to an existing address, and setting or resetting the option after the **LPWSPBind** has no effect on this or any other socket.

</dd> <dt>

<span id="SO_SNDBUF"></span><span id="so_sndbuf"></span>SO_SNDBUF
</dt> <dd>

When a Windows Sockets implementation supports the **SO_RCVBUF** and **SO_SNDBUF** options, a Windows Sockets SPI client can request different buffer sizes (larger or smaller). The call can succeed even though the service provider did not make available the entire amount requested. A Windows Sockets SPI client must call <b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspgetsockopt">LPWSPGetSockopt</a></b> with the same option to verify the buffer size actually provided.

</dd> <dt>

<span id="PVD_CONFIG"></span><span id="pvd_config"></span>PVD_CONFIG
</dt> <dd>

This object stores the configuration information for the service provider associated with socket <i>s</i>. The exact format of this data structure is service provider specific.

## -see-also

<b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspbind">LPWSPBind</a></b>
   

<b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspeventselect">LPWSPEventSelect</a></b>   

<b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspgetsockopt">LPWSPGetSockopt</a></b>
   

<b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspioctl">LPWSPIoctl</a></b>
   

<a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspsocket">LPWSPSocket</a>

