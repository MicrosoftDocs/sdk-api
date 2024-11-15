---
UID: NC:ws2spi.LPWSPGETSOCKOPT
title: LPWSPGETSOCKOPT
description: The LPWSPGetSockOpt function retrieves a socket option.
tech.root: winsock
helpviewer_keywords: ["LPWSPGETSOCKOPT"]
ms.date: 9/12/2019
ms.keywords: LPWSPGETSOCKOPT
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
 - LPWSPGETSOCKOPT
f1_keywords:
 - LPWSPGETSOCKOPT
 - ws2spi/LPWSPGETSOCKOPT
---

## -description

The **LPWSPGetSockOpt** function retrieves a socket option.

## -parameters

### -param s

A descriptor identifying a socket.

### -param level

The level at which the option is defined; the supported levels include <b><a href="/windows/win32/winsock/sol-socket-socket-options">SOL_SOCKET</a></b>. (See annex for more protocol-specific levels.)

### -param optname

The socket option for which the value is to be retrieved.

### -param optval

A pointer to the buffer in which the value for the requested option is to be returned.

### -param optlen

A pointer to the size, in bytes, of the <i>optval</i> buffer.

### -param lpErrno

A pointer to the error code.

## -returns

If no error occurs, **LPWSPGetSockOpt** returns zero. Otherwise, a value of SOCKET_ERROR is returned, and a specific error code is available in <i>lpErrno</i>.

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
One of the <i>optval</i> or the <i>optlen</i> parameters is not a valid part of the user address space, or the <i>optlen</i> parameter is too small.  
</td>
</tr>

<tr>
<td width="40%">
<dl>                                              
<dt><a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAEINVAL">WSAEINVAL</a></dt>
</dl>
</td>
<td width="60%">
The <i>level</i> is unknown or invalid.
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
<dt><a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAENOPROTOOPT">WSAENOPROTOOPT</a></dt>
</dl>
</td>
<td width="60%">
Option is unknown or unsupported by the indicated protocol family.
</td>
</tr>

<tr>
<td width="40%">
<dl>                                              
<dt><a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAENOTSOCK">WSAENOTSOCK</a></dt>
</dl>
</td>
<td width="60%">
The descriptor is not a socket.
</td>
</tr>
</table>

## -remarks

The **LPWSPGetSockOpt** function retrieves the current value for a socket option associated with a socket of any type, in any state, and stores the result in <i>optval</i>. Options can exist at multiple protocol levels, but they are always present at the uppermost socket' level. Options affect socket operations, such as the routing of packets and OOB data transfer.

The value associated with the selected option is returned in the buffer <i>optval</i>. The integer pointed to by <i>optlen</i> should originally contain the size of this buffer; on return, it will be set to the size of the value returned. For SO_LINGER, this will be the size of a structure linger; for most other options it will be the size of an integer.

The Windows Sockets SPI client is responsible for allocating any memory space pointed to directly or indirectly by any of the parameters it specifies.

If the option was never set with <b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspsetsockopt">LPWSPSetSockOpt</a></b>, then **LPWSPGetSockOpt** returns the default value for the option.

For more information on socket options, see <b><a href="/windows/win32/winsock/socket-options">Socket Options</a></b>.

### level = SOL_SOCKET



| Value                                 | Type                                                      | Meaning                                                                                                                                                                                                                                                             | Default                                                                 |
|---------------------------------------|-----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| SO_ACCEPTCONN                        | BOOL                                                      | The socket is listening through <b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwsplisten">LPWSPListen</a></b>.                                                                                                                                                                                                   | **FALSE** unless a <b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwsplisten">LPWSPListen</a></b> has been performed. |
| SO_BROADCAST                         | BOOL                                                      | The socket is configured for the transmission and receipt of broadcast messages.                                                                                                                                                                                    | **FALSE**                                                               |
| SO_DEBUG                             | BOOL                                                      | Debugging is enabled.                                                                                                                                                                                                                                               | **FALSE**                                                               |
| SO_DONTLINGER                        | BOOL                                                      | If true, the SO_LINGER option is disabled.                                                                                                                                                                                                                         | **TRUE**                                                                |
| SO_DONTROUTE                         | BOOL                                                      | Routing is disabled. Setting this socket option succeeds but is ignored on AF_INET sockets; fails on AF_INET6 sockets with <a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAENOPROTOOPT">WSAENOPROTOOPT</a> . This option is not supported on ATM sockets (results in an error). | **FALSE**                                                               |
| SO_ERROR                             | integer                                                   | Retrieves error status and clears.                                                                                                                                                                                                                                  | 0                                                                       |
| SO_GROUP_ID                         | GROUP                                                     | Reserved.                                                                                                                                                                                                                                                           | Null                                                                    |
| SO_GROUP_PRIORITY                   | integer                                                   | Reserved.                                                                                                                                                                                                                                                           | 0                                                                       |
| <b><a href="/windows/win32/winsock/so-keepalive">SO_KEEPALIVE</a></b> | BOOL                                                      | Keepalives are being sent. Not supported on ATM sockets (results in an error).                                                                                                                                                                                      | **FALSE**                                                               |
| SO_LINGER                            | <b><a href="/windows/win32/api/winsock2/ns-winsock2-linger">LINGER</a></b> structure                      | Returns the current linger options.                                                                                                                                                                                                                                 | 1 is on (default), 0 is off                                             |
| SO_MAX_MSG_SIZE                    | unsigned integer                                          | The maximum size of a message for message-oriented socket types (for example, SOCK_DGRAM). Has no meaning for stream oriented sockets.                                                                                                                             | Implementation dependent                                                |
| SO_OOBINLINE                         | BOOL                                                      | OOB data is being received in the normal data stream.                                                                                                                                                                                                               | **FALSE**                                                               |
| SO_PROTOCOL_INFO                    | <b><a href="/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa">WSAPROTOCOL_INFO</a></b> structure | A description of the protocol information for the protocol that is bound to this socket.                                                                                                                                                                            | Protocol dependent                                                      |
| SO_RCVBUF                            | integer                                                   | The total per-socket buffer space reserved for receives. This is unrelated to SO_MAX_MSG_SIZE and does not necessarily correspond to the size of the TCP receive window.                                                                                         | Implementation dependent                                                |
| SO_REUSEADDR                         | BOOL                                                      | The socket can be bound to an address that is already in use. This option is not applicable on ATM sockets.                                                                                                                                                         | **FALSE**.                                                              |
| SO_SNDBUF                            | integer                                                   | The total per-socket buffer space reserved for sends. This is unrelated to SO_MAX_MSG_SIZE and does not necessarily correspond to the size of a TCP send window.                                                                                                 | Implementation dependent                                                |
| SO_TYPE                              | integer                                                   | The type of socket (for example, SOCK_STREAM).                                                                                                                                                                                                                     | As created with <b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspsocket">LPWSPSocket</a>">LPWSPSocket</a></b>                              |
| PVD_CONFIG                           | Service Provider Dependent                                | An opaque data structure object from the service provider associated with socket <i>s</i>. This object stores the current configuration information of the service provider. The exact format of this data structure is service provider-specific.                       | Implementation dependent                                                |



 

Calling **LPWSPGetSockOpt** with an unsupported option will result in an error code of <a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAENOPROTOOPT">WSAENOPROTOOPT</a>  being returned in <i>lpErrno</i>.

<dl> <dt>

<span id="SO_DEBUG"></span><span id="so_debug"></span>SO_DEBUG
</dt> <dd>

Windows Sockets service providers are encouraged (but not required) to supply output debug information if the SO_DEBUG option is set by a Windows Sockets SPI client. The mechanism for generating the debug information and the form it takes are beyond the scope of this specification.

</dd> <dt>

<span id="SO_ERROR"></span><span id="so_error"></span>SO_ERROR
</dt> <dd>

The SO_ERROR option returns and resets the per-socket-based error code (that is not necessarily the same as the per-thread-error code that is maintained by the WS2_32.DLL). A successful Windows Sockets call on the socket does not reset the socket-based error code returned by the SO_ERROR option.

</dd> <dt>

<span id="SO_GROUP_ID"></span><span id="so_group_id"></span>SO_GROUP_ID
</dt> <dd>

Reserved. This value should be **NULL**.

</dd> <dt>

<span id="SO_GROUP_PRIORITY"></span><span id="so_group_priority"></span>SO_GROUP_PRIORITY
</dt> <dd>

Reserved.

</dd> <dt>

<span id="SO_KEEPALIVE"></span><span id="so_keepalive"></span><b><a href="/windows/win32/winsock/so-keepalive">SO_KEEPALIVE</a></b>
</dt> <dd>

A Windows Sockets SPI client can request that a TCP/IP service provider enable the use of keep-alive packets on TCP connections by turning on the <b><a href="/windows/win32/winsock/so-keepalive">SO_KEEPALIVE</a></b> socket option. A Windows Sockets provider need not support the use of keep-alives: if it does, the precise semantics are implementation specific but should conform to section 4.2.3.6 of RFC 1122: <i>Requirements for Internet Hosts—Communication Layers</i>. (This resource may only be available in English.) If a connection is dropped as the result of keep-alives, the error code <a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAENETRESET">WSAENETRESET</a>  is returned to any calls in progress on the socket, and any subsequent calls will fail with <a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAENOTCONN">WSAENOTCONN</a> .

</dd> <dt>

<span id="SO_LINGER"></span><span id="so_linger"></span>SO_LINGER
</dt> <dd>

SO_LINGER controls the action taken when unsent data is queued on a socket and a <b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspclosesocket">LPWSPCloseSocket</a></b> is performed. See **LPWSPCloseSocket** for a description of the way in which the SO_LINGER settings affect the semantics of **LPWSPCloseSocket**. The Windows Sockets SPI client obtains the desired behavior by creating a <b><a href="/windows/win32/api/winsock2/ns-winsock2-linger">LINGER</a></b> structure (pointed to by the *<i>optval</i>* parameter) with the following elements:


```C++
}
```



</dd> <dt>

<span id="SO_MAX_MSG_SIZE"></span><span id="so_max_msg_size"></span>SO_MAX_MSG_SIZE
</dt> <dd>

This is a get-only socket option, which indicates the maximum size of an outbound send message for message-oriented socket types (for example, SOCK_DGRAM) as implemented by the service provider. It has no meaning for byte stream-oriented sockets. There is no provision to determine the maximum inbound message size.

</dd> <dt>

<span id="SO_PROTOCOL_INFOW"></span><span id="so_protocol_infow"></span>SO_PROTOCOL_INFOW
</dt> <dd>

This is a get-only option that supplies the <b><a href="/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa">WSAPROTOCOL_INFO</a></b> structure associated with this socket. See <b><a href="/windows/win32/api/ws2spi/nf-ws2spi-wscenumprotocols">WSCEnumProtocols</a></b> for more information about this structure.

</dd> <dt>

<span id="SO_SNDBUF"></span><span id="so_sndbuf"></span>SO_SNDBUF
</dt> <dd>

When a Windows Sockets service provider supports the SO_RCVBUF and SO_SNDBUF options, a Windows Sockets SPI client can use <b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspsetsockopt">LPWSPSetSockOpt</a></b> to request different buffer sizes (larger or smaller). The call can succeed even though the service provider did not make available the entire amount requested. A Windows Sockets SPI client must call this function with the same option to check the buffer size actually provided.

</dd> <dt>

<span id="SO_REUSEADDR"></span><span id="so_reuseaddr"></span>SO_REUSEADDR
</dt> <dd>

By default, a socket cannot be bound (see <b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspbind">LPWSPBind</a></b>) to a local address that is already in use. On occasion, however, it may be desirable to reuse an address in this way. Since every connection is uniquely identified by the combination of local and remote addresses, there is no problem with having two sockets bound to the same local address as long as the remote addresses are different. To inform the Windows Sockets provider that a **LPWSPBind** on a socket should be allowed to bind to a local address that is already in use by another socket, the Windows Sockets SPI client should set the SO_REUSEADDR socket option for the socket before issuing the **LPWSPBind**. Note that the option is interpreted only at the time of the **LPWSPBind**. It is therefore unnecessary (but harmless) to set the option on a socket that is not to be bound to an existing address, and setting or resetting the option after the **LPWSPBind** has no effect on this or any other socket.

</dd> <dt>

<span id="PVD_CONFIG"></span><span id="pvd_config"></span>PVD_CONFIG
</dt> <dd>

This option retrieves an opaque data structure object from the service provider associated with socket <i>s</i>. This object stores the current configuration information of the service provider. The exact format of this data structure is service-provider specific.

## -see-also

<b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspsetsockopt">LPWSPSetSockOpt</a></b>
   

<a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspsocket">LPWSPSocket</a>

