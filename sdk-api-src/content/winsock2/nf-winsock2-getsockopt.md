---
UID: NF:winsock2.getsockopt
title: getsockopt function (winsock2.h)
description: The getsockopt function retrieves the current value for a socket option associated with a socket of any type, in any state, and stores the result in optval.  
helpviewer_keywords: ["_win32_getsockopt_2","getsockopt","getsockopt function [Winsock]","winsock.getsockopt_2","winsock/getsockopt"]
old-location: winsock\getsockopt_2.htm
tech.root: WinSock
ms.assetid: 25bc511d-7a9f-41c1-8983-1af1e3f8bf2d
ms.date: 08/03/2022
ms.keywords: _win32_getsockopt_2, getsockopt, getsockopt function [Winsock], winsock.getsockopt_2, winsock/getsockopt
req.header: winsock2.h
req.include-header: Winsock2.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1, Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
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
ms.custom: 19H1
f1_keywords:
 - getsockopt
 - winsock2/getsockopt
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ws2_32.dll
 - wsock32.dll
api_name:
 - getsockopt
---

## -description

The <b>getsockopt</b> function retrieves a socket option.

## -parameters

### -param s [in]

A descriptor identifying a socket.

### -param level [in]

The level at which the option is defined. Example:  <a href="/windows/desktop/WinSock/sol-socket-socket-options">SOL_SOCKET</a>.

### -param optname [in]

The socket option for which the value is to be retrieved. Example: <a href="/windows/desktop/WinSock/socket-options-and-ioctls-2">SO_ACCEPTCONN</a>. The <i>optname</i> value must be a socket option defined within the specified <i>level</i>, or behavior is undefined.

### -param optval [out]

A pointer to the buffer in which the value for the requested option is to be returned.

### -param optlen [in, out]

A pointer to the size, in bytes, of the <i>optval</i> buffer.

## -returns

If no error occurs, 
<b>getsockopt</b> returns zero. Otherwise, a value of SOCKET_ERROR is returned, and a specific error code can be retrieved by calling 
<a href="/windows/desktop/api/winsock/nf-winsock-wsagetlasterror">WSAGetLastError</a>.

<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSANOTINITIALISED</a></b></dt>
</dl>
</td>
<td width="60%">
A successful 
<a href="/windows/desktop/api/winsock/nf-winsock-wsastartup">WSAStartup</a> call must occur before using this function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAENETDOWN</a></b></dt>
</dl>
</td>
<td width="60%">
<div class="alert"><b>Note</b>  The network subsystem has failed.</div>
<div> </div>
</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEFAULT</a></b></dt>
</dl>
</td>
<td width="60%">
One of the <i>optval</i> or the <i>optlen</i> parameters is not a valid part of the user address space, or the <i>optlen</i> parameter is too small.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEINPROGRESS</a></b></dt>
</dl>
</td>
<td width="60%">
A blocking Windows Sockets 1.1 call is in progress, or the service provider is still processing a callback function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEINVAL</a></b></dt>
</dl>
</td>
<td width="60%">
The <i>level</i> parameter is unknown or invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAENOPROTOOPT</a></b></dt>
</dl>
</td>
<td width="60%">
The option is unknown or unsupported by the indicated protocol family.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAENOTSOCK</a></b></dt>
</dl>
</td>
<td width="60%">
The descriptor is not a socket.

</td>
</tr>
</table>

## -remarks

The 
<b>getsockopt</b> function retrieves the current value for a socket option associated with a socket of any type, in any state, and stores the result in <i>optval</i>. Options can exist at multiple protocol levels, but they are always present at the uppermost socket level. Options affect socket operations, such as the packet routing and OOB data transfer.

The value associated with the selected option is returned in the buffer <i>optval</i>. The integer pointed to by <i>optlen</i> should originally contain the size of this buffer; on return, it will be set to the size of the value returned. For SO_LINGER, this will be the size of a 
<a href="/windows/desktop/api/winsock/ns-winsock-linger">LINGER</a> structure. For most other options, it will be the size of an integer.

The application is responsible for allocating any memory space pointed to directly or indirectly by any of the parameters it specified.

If the option was never set with 
<a href="/windows/desktop/api/winsock/nf-winsock-setsockopt">setsockopt</a>, then 
<b>getsockopt</b> returns the default value for the option.

The following options are supported for 
<b>getsockopt</b>. The Type column identifies the type of data addressed by <i>optval</i>.

For more information on socket options, see <a href="/windows/desktop/WinSock/socket-options">Socket Options</a>.

The following table of value for the <i>optname</i> parameter are valid when the <i>level</i> parameter is set to <b>SOL_SOCKET</b>.


<table>
<tr>
<th>Value</th>
<th>Type</th>
<th>Meaning</th>
</tr>
<tr>
<td>SO_ACCEPTCONN</td>
<td>BOOL</td>
<td>The socket is listening.</td>
</tr>
<tr>
<td>SO_BROADCAST</td>
<td>BOOL</td>
<td>The socket is configured for the transmission and receipt of broadcast messages.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/WinSock/so-bsp-state">SO_BSP_STATE</a>
</td>
<td>
<a href="/windows/desktop/api/nspapi/ns-nspapi-csaddr_info">CSADDR_INFO</a>
</td>
<td>Returns the local address, local port, remote address, remote port, socket type, and protocol used by a socket.</td>
</tr>
<tr>
<td>SO_CONDITIONAL_ACCEPT</td>
<td>BOOL</td>
<td>Returns current socket state, either from a previous call to 
<a href="/windows/desktop/api/winsock/nf-winsock-setsockopt">setsockopt</a> or the system default.</td>
</tr>
<tr>
<td>SO_CONNECT_TIME</td>
<td>DWORD</td>
<td>Returns the number of seconds a socket has been connected. This socket option is valid for connection oriented protocols only. </td>
</tr>
<tr>
<td>SO_DEBUG</td>
<td>BOOL</td>
<td>Debugging is enabled.</td>
</tr>
<tr>
<td>SO_DONTLINGER</td>
<td>BOOL</td>
<td>If <b>TRUE</b>, the SO_LINGER option is disabled.</td>
</tr>
<tr>
<td>SO_DONTROUTE</td>
<td>BOOL</td>
<td>Routing is disabled. Setting this succeeds but is ignored on AF_INET sockets; fails on AF_INET6 sockets with <a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAENOPROTOOPT</a>. This option is not supported on ATM sockets.</td>
</tr>
<tr>
<td>SO_ERROR</td>
<td>int</td>
<td>Retrieves error status and clear.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/WinSock/so-exclusiveaddruse">SO_EXCLUSIVEADDRUSE</a>
</td>
<td>BOOL</td>
<td>Prevents any other socket from binding to the same address and port. This option must be set before calling the <a href="/windows/desktop/api/winsock/nf-winsock-bind">bind</a> function.</td>
</tr>
<tr>
<td>SO_GROUP_ID</td>
<td>GROUP</td>
<td>Reserved.</td>
</tr>
<tr>
<td>SO_GROUP_PRIORITY</td>
<td>int</td>
<td>Reserved.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/WinSock/so-keepalive">SO_KEEPALIVE</a>
</td>
<td>BOOL</td>
<td>Keep-alives are being sent. Not supported on ATM sockets.</td>
</tr>
<tr>
<td>SO_LINGER</td>
<td>
<a href="/windows/desktop/api/winsock/ns-winsock-linger">LINGER</a> structure</td>
<td>Returns the current linger options.</td>
</tr>
<tr>
<td>SO_MAX_MSG_SIZE</td>
<td>unsigned int</td>
<td>The maximum size of a message for message-oriented socket types (for example, SOCK_DGRAM). Has no meaning for stream oriented sockets.</td>
</tr>
<tr>
<td>SO_OOBINLINE</td>
<td>BOOL</td>
<td>OOB data is being received in the normal data stream. (See section 
<a href="/windows/desktop/WinSock/windows-sockets-1-1-blocking-routines-and-einprogress-2">Windows Sockets 1.1 Blocking Routines and EINPROGRESS</a> for a discussion of this topic.)</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/WinSock/so-port-scalability">SO_PORT_SCALABILITY</a>
</td>
<td>BOOL</td>
<td>Enables local port scalability for a socket by allowing port allocation to be maximized by allocating wildcard ports multiple times for different local address port pairs on a local machine.</td>
</tr>
<tr>
<td>SO_PROTOCOL_INFO</td>
<td>
<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaprotocol_infoa">WSAPROTOCOL_INFO</a>
</td>
<td>A description of the protocol information for the protocol that is bound to this socket.</td>
</tr>
<tr>
<td>SO_RCVBUF</td>
<td>int</td>
<td>The total per-socket buffer space reserved for receives. This is unrelated to SO_MAX_MSG_SIZE and does not necessarily correspond to the size of the TCP receive window.</td>
</tr>
<tr>
<td>SO_REUSEADDR</td>
<td>BOOL</td>
<td>The socket can be bound to an address which is already in use. Not applicable for ATM sockets.</td>
</tr>
<tr>
<td>SO_SNDBUF</td>
<td>int</td>
<td>The total per-socket buffer space reserved for sends. This is unrelated to SO_MAX_MSG_SIZE and does not necessarily correspond to the size of a TCP send window.</td>
</tr>
<tr>
<td>SO_TYPE</td>
<td>int</td>
<td>The type of the socket (for example, SOCK_STREAM).</td>
</tr>
<tr>
<td>PVD_CONFIG</td>
<td>Service Provider Dependent</td>
<td>An opaque data structure object from the service provider associated with socket <i>s</i>. This object stores the current configuration information of the service provider. The exact format of this data structure is service provider specific.</td>
</tr>
</table>
 


<i>level</i> = <b>IPPROTO_TCP</b>

See **TCP_NODELAY** in [IPPROTO_TCP socket options](/windows/desktop/WinSock/ipproto-tcp-socket-options). Also see that topic for more complete and detailed information about socket options for <i>level</i> = <b>IPPROTO_TCP</b>.
 



The following table of value for the <i>optname</i> parameter are valid when the <i>level</i> parameter is set to <b>NSPROTO_IPX</b>.

<div class="alert"><b>Note</b>  Windows NT supports all IPX options. Windows Me, Windows 98, and Windows 95 support only the following options:<dl>
<dd>IPX_PTYPE</dd>
<dd>IPX_FILTERPTYPE</dd>
<dd>IPX_DSTYPE</dd>
<dd>IPX_RECVHDR</dd>
<dd>IPX_MAXSIZE</dd>
<dd>IPX_ADDRESS</dd>
</dl>
</div>
<div> </div>

<table>
<tr>
<th>Value</th>
<th>Type</th>
<th>Meaning</th>
</tr>
<tr>
<td>IPX_PTYPE</td>
<td>int</td>
<td>Retrieves the IPX packet type.</td>
</tr>
<tr>
<td>IPX_FILTERPTYPE</td>
<td>int</td>
<td>Retrieves the receive filter packet type</td>
</tr>
<tr>
<td>IPX_DSTYPE</td>
<td>int</td>
<td>Obtains the value of the data stream field in the SPX header on every packet sent.</td>
</tr>
<tr>
<td>IPX_EXTENDED_ADDRESS</td>
<td>BOOL</td>
<td>Finds out whether extended addressing is enabled.</td>
</tr>
<tr>
<td>IPX_RECVHDR</td>
<td>BOOL</td>
<td>Finds out whether the protocol header is sent up on all receive headers.</td>
</tr>
<tr>
<td>IPX_MAXSIZE</td>
<td>int</td>
<td>Obtains the maximum data size that can be sent.</td>
</tr>
<tr>
<td>IPX_ADDRESS</td>
<td>
<a href="/windows/desktop/api/wsnwlink/ns-wsnwlink-ipx_address_data">IPX_ADDRESS_DATA</a> structure</td>
<td>Obtains information about a specific adapter to which IPX is bound. Adapter numbering is base zero. The <b>adapternum</b> member is filled in upon return.</td>
</tr>
<tr>
<td>IPX_GETNETINFO</td>
<td>
<a href="/windows/desktop/api/wsnwlink/ns-wsnwlink-ipx_netnum_data">IPX_NETNUM_DATA</a> structure</td>
<td>Obtains information about a specific IPX network number. If not available in the cache, uses RIP to obtain information.</td>
</tr>
<tr>
<td>IPX_GETNETINFO_NORIP</td>
<td>
<a href="/windows/desktop/api/wsnwlink/ns-wsnwlink-ipx_netnum_data">IPX_NETNUM_DATA</a> structure</td>
<td>Obtains information about a specific IPX network number. If not available in the cache, will not use RIP to obtain information, and returns error.</td>
</tr>
<tr>
<td>IPX_SPXGETCONNECTIONSTATUS</td>
<td>
<a href="/windows/desktop/api/wsnwlink/ns-wsnwlink-ipx_spxconnstatus_data">IPX_SPXCONNSTATUS_DATA</a> structure</td>
<td>Retrieves information about a connected SPX socket.</td>
</tr>
<tr>
<td>IPX_ADDRESS_NOTIFY</td>
<td>
<a href="/windows/desktop/api/wsnwlink/ns-wsnwlink-ipx_address_data">IPX_ADDRESS_DATA</a> structure</td>
<td>Retrieves status notification when changes occur on an adapter to which IPX is bound.</td>
</tr>
<tr>
<td>IPX_MAX_ADAPTER_NUM</td>
<td>int</td>
<td>Retrieves maximum number of adapters present, numbered as base zero.</td>
</tr>
<tr>
<td>IPX_RERIPNETNUMBER</td>
<td>
<a href="/windows/desktop/api/wsnwlink/ns-wsnwlink-ipx_netnum_data">IPX_NETNUM_DATA</a> structure</td>
<td>Similar to IPX_GETNETINFO, but forces IPX to use RIP for resolution, even if the network information is in the local cache.</td>
</tr>
<tr>
<td>IPX_IMMEDIATESPXACK</td>
<td>BOOL</td>
<td>Directs SPX connections not to delay before sending an ACK. Applications without back-and-forth traffic should set this to <b>TRUE</b> to increase performance.</td>
</tr>
<tr>
<td>TCP_MAXSEG</td>
<td>int</td>
<td>Receives TCP maximum-segment size. Supported in Windows 10 and newer versions.</td>
</tr>
</table>
 



The following table lists value for the <i>optname</i> that represent BSD socket options that are not supported by the <b>getsockopt</b> function.
		    <table>
<tr>
<th>Value</th>
<th>Type</th>
<th>Meaning</th>
</tr>
<tr>
<td>SO_RCVLOWAT</td>
<td>int</td>
<td>Receives low watermark.</td>
</tr>
<tr>
<td>SO_RCVTIMEO</td>
<td>int</td>
<td>Receives time-out.</td>
</tr>
<tr>
<td>SO_SNDLOWAT</td>
<td>int</td>
<td>Sends low watermark.</td>
</tr>
<tr>
<td>SO_SNDTIMEO</td>
<td>int</td>
<td>Sends time-out.</td>
</tr>
<tr>
<td>TCP_MAXSEG</td>
<td>int</td>
<td>Receives TCP maximum-segment size. Not supported in versions before Windows 10.</td>
</tr>
</table>
 




<div class="alert"><b>Note</b>  When using the 
<a href="/windows/desktop/api/winsock/nf-winsock-recv">recv</a> function, if no data arrives during the period specified in SO_RCVTIMEO, the 
<b>recv</b> function completes. In Windows versions prior to Windows 2000, any data received subsequently fails with <a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAETIMEDOUT</a>. In Windows 2000 and later, if no data arrives within the period specified in SO_RCVTIMEO, the 
<b>recv</b> function returns WSAETIMEDOUT, and if data is received, 
<b>recv</b> returns SUCCESS.</div>
<div> </div>


Calling 
<b>getsockopt</b> with an unsupported option will result in an error code of 
<a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAENOPROTOOPT</a> being returned from 
<a href="/windows/desktop/api/winsock/nf-winsock-wsagetlasterror">WSAGetLastError</a>.

More detailed information  on some of the socket options for the <i>optname</i> parameter supported by the <b>getsockopt</b> function are listed below.




<dl>
<dt><a id="SO_CONNECT_TIME"></a><a id="so_connect_time"></a>SO_CONNECT_TIME</dt>
<dd>
This option returns the number of seconds a socket has been connected. This option is valid for connection oriented protocols only.

The SO_CONNECT_TIME option can be used with the <b>getsockopt</b> function to check 
    whether a connection has been established. This option can also be used  while a <a href="/windows/desktop/api/mswsock/nc-mswsock-lpfn_connectex">ConnectEx</a> function call is in progress.
    If a connection is established, the SO_CONNECT_TIME option can determine how long the connection has
    been established. If the socket is not connected, the <b>getsockopt</b> returns
    SOCKET_ERROR. Checking a connection like this is necessary to see if
    connections that have been established for a while, without sending any
    data. It is recommended that applications terminate these connections. 

</dd>
<dt><a id="SO_DEBUG"></a><a id="so_debug"></a>SO_DEBUG</dt>
<dd>
<div class="alert"><b>Note</b>  Windows Sockets service providers are encouraged (but not required) to supply output debug information if the SO_DEBUG option is set by an application. The mechanism for generating the debug information and the form it takes are beyond the scope of this document.</div>
<div> </div>
</dd>
<dt><a id="SO_ERROR"></a><a id="so_error"></a>SO_ERROR</dt>
<dd>
The SO_ERROR option returns and resets the per socket–based error code, which is different from the per thread based–error code that is handled using the 
<a href="/windows/desktop/api/winsock/nf-winsock-wsagetlasterror">WSAGetLastError</a> and 
<a href="/windows/desktop/api/winsock/nf-winsock-wsasetlasterror">WSASetLastError</a> function calls. A successful call using the socket does not reset the socket based error code returned by the SO_ERROR option.

</dd>
<dt><a id="SO_EXCLUSIVEADDRUSE"></a><a id="so_exclusiveaddruse"></a>SO_EXCLUSIVEADDRUSE</dt>
<dd>
Prevents any other socket from binding to the same address and port. This option must be set before calling the <a href="/windows/desktop/api/winsock/nf-winsock-bind">bind</a> function. See the <a href="/windows/desktop/WinSock/so-exclusiveaddruse">SO_EXCLUSIVEADDRUSE</a> reference for more information.

</dd>
<dt><a id="SO_GROUP_ID"></a><a id="so_group_id"></a>SO_GROUP_ID</dt>
<dd>
<div class="alert"><b>Note</b>  This option is reserved. This option is also exclusive to 
<b>getsockopt</b>; the value should be <b>NULL</b>.</div>
<div> </div>
</dd>
<dt><a id="SO_GROUP_PRIORITY"></a><a id="so_group_priority"></a>SO_GROUP_PRIORITY</dt>
<dd>
This option is reserved. Group priority indicates the priority of the specified socket relative to other sockets within the socket group. Values are nonnegative integers, with zero corresponding to the highest priority. Priority values represent a hint to the underlying service provider about how potentially scarce resources should be allocated. For example, whenever two or more sockets are both ready to transmit data, the highest priority socket (lowest value for SO_GROUP_PRIORITY) should be serviced first, with the remainder serviced in turn according to their relative priorities.

The WSAENOPROTOOPT error code is indicated for nongroup sockets or for service providers that do not support group sockets.

</dd>
<dt><a id="SO_KEEPALIVE"></a><a id="so_keepalive"></a><a href="/windows/desktop/WinSock/so-keepalive">SO_KEEPALIVE</a>
</dt>
<dd>
An application can request that a TCP/IP service provider enable the use of keep-alive packets on TCP  connections by turning on the SO_KEEPALIVE socket option. This option queries the current value of the keep-alive option on a socket. A Windows Sockets provider need not support the use of keep-alive: if it does, the precise semantics are implementation-specific but should conform to section 4.2.3.6 on the <i>Requirements for Internet Hosts—Communication Layers</i> specified in RFC 1122 available at the <a href="https://www.ietf.org/rfc/rfc1122.txt">IETF website</a>.  If a connection is dropped as the result of keep-alives the error code 
<a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAENETRESET</a> is returned to any calls in progress on the socket, and any subsequent calls will fail with 
<a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAENOTCONN</a>. <a href="/windows/desktop/WinSock/so-keepalive">SO_KEEPALIVE</a> is not supported on ATM sockets, and requests to enable the use of keep-alive packets on an ATM socket results in an error being returned by the socket.

</dd>
<dt><a id="SO_LINGER"></a><a id="so_linger"></a>SO_LINGER</dt>
<dd>
SO_LINGER controls the action taken when unsent data is queued on a socket and a 
<a href="/windows/desktop/api/winsock/nf-winsock-closesocket">closesocket</a> is performed. See 
<b>closesocket</b> for a description of the way in which the SO_LINGER settings affect the semantics of 
<b>closesocket</b>. The application gets the current behavior by retrieving a 
<a href="/windows/desktop/api/winsock/ns-winsock-linger">LINGER</a> structure (pointed to by the <i>optval</i> parameter).

</dd>
<dt><a id="SO_MAX_MSG_SIZE"></a><a id="so_max_msg_size"></a>SO_MAX_MSG_SIZE</dt>
<dd>
This is a get-only socket option that indicates the maximum outbound (send) size of a message for message-oriented socket types (for example, SOCK_DGRAM) as implemented by a particular service provider. It has no meaning for byte stream oriented sockets. There is no provision to find out the maximum inbound–message size.

</dd>
<dt><a id="SO_PROTOCOL_INFO"></a><a id="so_protocol_info"></a>SO_PROTOCOL_INFO</dt>
<dd>
This is a get-only option that supplies the 
<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaprotocol_infoa">WSAPROTOCOL_INFO</a> structure associated with this socket. See 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaenumprotocolsa">WSAEnumProtocols</a> for more information about this structure.

</dd>
<dt><a id="SO_SNDBUF"></a><a id="so_sndbuf"></a>SO_SNDBUF</dt>
<dd>
When a Windows Sockets implementation supports the SO_RCVBUF and SO_SNDBUF options, an application can request different buffer sizes (larger or smaller). The call to 
<a href="/windows/desktop/api/winsock/nf-winsock-setsockopt">setsockopt</a> can succeed even if the implementation did not provide the whole amount requested. An application must call this function with the same option to check the buffer size actually provided.

</dd>
<dt><a id="SO_REUSEADDR"></a><a id="so_reuseaddr"></a>SO_REUSEADDR</dt>
<dd>
By default, a socket cannot be bound (see 
<a href="/windows/desktop/api/winsock/nf-winsock-bind">bind</a>) to a local address that is already in use. On occasion, however, it can be necessary to reuse an address in this way. Because every connection is uniquely identified by the combination of local and remote addresses, there is no problem with having two sockets bound to the same local address as long as the remote addresses are different. To inform the Windows Sockets provider that a 
<b>bind</b> on a socket should not be disallowed because the desired address is already in use by another socket, the application should set the SO_REUSEADDR socket option for the socket before issuing the 
<b>bind</b>. Note that the option is interpreted only at the time of the 
<b>bind</b>: it is therefore unnecessary (but harmless) to set the option on a socket that is not to be bound to an existing address, and setting or resetting the option after the 
<b>bind</b> has no effect on this or any other socket. SO_REUSEADDR is not applicable for ATM sockets, and although requests to reuse and address do not result in an error, they have no effect on when an ATM socket is in use.

</dd>
<dt><a id="PVD_CONFIG"></a><a id="pvd_config"></a>PVD_CONFIG</dt>
<dd>
This option retrieves an opaque data structure object from the service provider associated with socket <i>s</i>. This object stores the current configuration information of the service provider. The exact format of this data structure is service provider specific.

</dd>
<dt><a id="TCP_NODELAY"></a><a id="tcp_nodelay"></a>TCP_NODELAY</dt>
<dd>
The TCP_NODELAY option is specific to TCP/IP service providers. The Nagle algorithm is disabled if the TCP_NODELAY option is enabled (and vice versa). The Nagle algorithm (described in RFC 896) is very effective in reducing the number of small packets sent by a host. The process involves buffering send data when there is unacknowledged data already in flight or buffering send data until a full-size packet can be sent. It is highly recommended that Windows Sockets implementations enable the Nagle Algorithm by default because, for the vast majority of application protocols, the Nagle Algorithm can deliver significant performance enhancements. However, for some applications this algorithm can impede performance, and 
<a href="/windows/desktop/api/winsock/nf-winsock-setsockopt">setsockopt</a> with the same option can be used to turn it off. These are applications where many small messages are sent, and the time delays between the messages are maintained.

</dd>
</dl>


<div class="alert"><b>Note</b>  When issuing a blocking Winsock call such as <b>getsockopt</b>, Winsock may need to wait for a network event before the call can complete. Winsock performs an alertable wait in this situation, which can be interrupted by an asynchronous procedure call (APC) scheduled on the same thread. Issuing another blocking Winsock call inside an APC that interrupted an ongoing blocking Winsock call on the same thread will lead to undefined behavior, and must never be attempted by Winsock clients. </div>
<div> </div>
<h3><a id="Example_Code"></a><a id="example_code"></a><a id="EXAMPLE_CODE"></a>Example Code</h3>
The following code sample demonstrates the use of the <b>getsockopt</b> function.


```cpp
#include <stdio.h>
#include "winsock2.h"
#include <windows.h>

void main() {

  //---------------------------------------
  // Declare variables
  WSADATA wsaData;
  SOCKET ListenSocket;
  sockaddr_in service;

  //---------------------------------------
  // Initialize Winsock
  int iResult = WSAStartup( MAKEWORD(2,2), &wsaData );
  if( iResult != NO_ERROR )
    printf("Error at WSAStartup\n");

  //---------------------------------------
  // Create a listening socket
  ListenSocket = socket( AF_INET, SOCK_STREAM, IPPROTO_TCP );
  if (ListenSocket == INVALID_SOCKET) {
    printf("Error at socket()\n");
    WSACleanup();
    return;
  }

  //---------------------------------------
  // Bind the socket to the local IP address
  // and port 27015
  hostent* thisHost;
  char* ip;
  u_short port;
  port = 27015;
  thisHost = gethostbyname("");
  ip = inet_ntoa (*(struct in_addr *)*thisHost->h_addr_list);

  service.sin_family = AF_INET;
  service.sin_addr.s_addr = inet_addr(ip);
  service.sin_port = htons(port);
 
  if ( bind( ListenSocket,(SOCKADDR*) &service, sizeof(service) )  == SOCKET_ERROR ) {
    printf("bind failed\n");
    closesocket(ListenSocket);
    return;
  }

  //---------------------------------------
  // Initialize variables and call getsockopt. 
  // The SO_ACCEPTCONN parameter is a socket option 
  // that tells the function to check whether the 
  // socket has been put in listening mode or not. 
  // The various socket options return different
  // information about the socket. This call should
  // return 0 to the optVal parameter, since the socket
  // is not in listening mode.
  int optVal;
  int optLen = sizeof(int);

  if (getsockopt(ListenSocket, 
    SOL_SOCKET, 
    SO_ACCEPTCONN, 
    (char*)&optVal, 
    &optLen) != SOCKET_ERROR)
    printf("SockOpt Value: %ld\n", optVal);

  //---------------------------------------
  // Put the listening socket in listening mode.
  if (listen( ListenSocket, 100 ) == SOCKET_ERROR) {
    printf("error listening\n");
  } 

  //---------------------------------------
  // Call getsockopt again to verify that 
  // the socket is in listening mode.
  if (getsockopt(ListenSocket, 
    SOL_SOCKET, 
    SO_ACCEPTCONN, 
    (char*)&optVal, 
    &optLen) != SOCKET_ERROR)
    printf("SockOpt Value: %ld\n", optVal);

  WSACleanup();
  return;
}

```


<h3><a id="Notes_for_IrDA_Sockets"></a><a id="notes_for_irda_sockets"></a><a id="NOTES_FOR_IRDA_SOCKETS"></a>Notes for IrDA Sockets</h3>

<ul>
<li>The Af_irda.h header file must be explicitly included.</li>
<li>Windows returns 
<a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAENETDOWN</a> to indicate the underlying transceiver driver failed to initialize with the IrDA protocol stack.</li>
<li>IrDA supports several special socket options:<table>
<tr>
<th>Value</th>
<th>Type</th>
<th>Meaning</th>
</tr>
<tr>
<td>IRLMP_ENUMDEVICES</td>
<td>*DEVICELIST</td>
<td>Describes devices in range.</td>
</tr>
<tr>
<td>IRLMP_IAS_QUERY</td>
<td>*IAS_QUERY</td>
<td>Retrieve IAS attributes.</td>
</tr>
</table>
 

</li>
</ul>


Before an IrDA socket connection can be initiated, a device address must be obtained by performing a 
<b>getsockopt</b>(,,IRLMP_ENUMDEVICES,,) function call, which returns a list of all available IrDA devices. A device address returned from the function call is copied into a 
<a href="/windows/desktop/api/af_irda/ns-af_irda-sockaddr_irda">SOCKADDR_IRDA</a> structure, which in turn is used by a subsequent call to the 
<a href="/windows/desktop/api/winsock2/nf-winsock2-connect">connect</a> function call.

Discovery can be performed in two ways:

<ol>
<li>
First, performing a getsockopt function call with the IRLMP_ENUMDEVICES option causes a single discovery to be run on each idle adapter. The list of discovered devices and cached devices (on active adapters) is returned immediately. 

The following code demonstrates this approach.


```cpp
#include <winsock2.h>
#include <ws2tcpip.h>
#include <af_irda.h>
#include <stdio.h>
#include <windows.h>

// link with Ws2_32.lib

int __cdecl main()
{

    //-----------------------------------------
    // Declare and initialize variables
    WSADATA wsaData;

    int iResult;
    int i;
    DWORD dwError;

    SOCKET Sock = INVALID_SOCKET;

#define DEVICE_LIST_LEN    10


    SOCKADDR_IRDA DestSockAddr = { AF_IRDA, 0, 0, 0, 0, "SampleIrDAService" };

    unsigned char DevListBuff[sizeof (DEVICELIST) -
                              sizeof (IRDA_DEVICE_INFO) +
                              (sizeof (IRDA_DEVICE_INFO) * DEVICE_LIST_LEN)];

    int DevListLen = sizeof (DevListBuff);
    PDEVICELIST pDevList;

    pDevList = (PDEVICELIST) & DevListBuff;

    // Initialize Winsock
    iResult = WSAStartup(MAKEWORD(2, 2), &wsaData);
    if (iResult != 0) {
        printf("WSAStartup failed: %d\n", iResult);
        return 1;
    }

    Sock = socket(AF_IRDA, SOCK_STREAM, 0);
    if (Sock == INVALID_SOCKET) {
        dwError = WSAGetLastError();
        printf
            ("socket failed trying to create an AF_IRDA socket with error %d\n",
             dwError);

        if (dwError == WSAEAFNOSUPPORT) {
            printf("Check that the local computer has an infrared device\n");
            printf
                ("and a device driver is installed for the infrared device\n");
        }
        WSACleanup();
        return 1;
    }
    // Sock is not in connected state
    iResult = getsockopt(Sock, SOL_IRLMP, IRLMP_ENUMDEVICES,
                         (char *) pDevList, &DevListLen);
    if (iResult == SOCKET_ERROR) {
        printf("getsockopt failed with error %d\n", WSAGetLastError());
        WSACleanup();
        return 1;
    }

    if (pDevList->numDevice == 0) {
        // no devices discovered or cached
        // not a bad idea to run a couple of times
        printf("No IRDA devices were discovered or cached\n");
    } else {
        // one per discovered device
        for (i = 0; i < (int) pDevList->numDevice; i++) {
            // typedef struct _IRDA_DEVICE_INFO
            // {
            //     u_char    irdaDeviceID[4];
            //     char      irdaDeviceName[22];
            //     u_char    irdaDeviceHints1;
            //     u_char    irdaDeviceHints2;
            //     u_char    irdaCharSet;
            // } _IRDA_DEVICE_INFO;

            // pDevList->Device[i]. see _IRDA_DEVICE_INFO for fields
            // display the device names and let the user select one
        }
    }

    // assume the user selected the first device [0]
    memcpy(&DestSockAddr.irdaDeviceID[0], &pDevList->Device[0].irdaDeviceID[0],
           4);

    iResult = connect(Sock, (const struct sockaddr *) &DestSockAddr,
                      sizeof (SOCKADDR_IRDA));
    if (iResult == SOCKET_ERROR) {
        printf("connect failed with error %d\n", WSAGetLastError());
    } else
        printf("connect to first IRDA device was successful\n");

    WSACleanup();
    return 0;
}

```


</li>
<li>The second approach to performing discovery of IrDA device addresses is to perform a lazy discovery; in this approach, the application is not notified until the discovered devices list changes from the last discovery run by the stack.</li>
</ol>
The <b>DEVICELIST</b> structure shown in the Type column in the previous table is an extendible array of device descriptions. IrDA fills in as many device descriptions as can fit in the specified buffer. The device description consists of a device identifier necessary to form a sockaddr_irda structure, and a displayable string describing the device.

The <b>IAS_QUERY</b> structure shown in the Type column in the previous table is used to retrieve a single attribute of a single class from a peer device's IAS database. The application specifies the device and class to query and the attribute and attribute type. Note that the device would have been obtained previously by a call to 
<b>getsockopt</b>(IRLMP_ENUMDEVICES). It is expected that the application allocates a buffer, of the necessary size, for the returned parameters.

Many level socket options are not meaningful to IrDA; only SO_LINGER and SO_DONTLINGER are specifically supported.

<b>Windows Phone 8:</b> This function is supported for Windows Phone Store apps on Windows Phone 8 and later.

<b>Windows 8.1</b> and <b>Windows Server 2012 R2</b>: This function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and later.

## -see-also

<a href="/windows/desktop/WinSock/ipproto-ip-socket-options">IPPROTO_IP Socket Options</a>



<a href="/windows/desktop/WinSock/ipproto-ipv6-socket-options">IPPROTO_IPV6 Socket Options</a>



<a href="/windows/desktop/WinSock/ipproto-rm-socket-options">IPPROTO_RM Socket Options</a>



<a href="/windows/desktop/WinSock/ipproto-tcp-socket-options">IPPROTO_TCP Socket Options</a>



<a href="/windows/desktop/WinSock/ipproto-udp-socket-options">IPPROTO_UDP Socket Options</a>



<a href="/windows/desktop/WinSock/nsproto-ipx-socket-options">NSPROTO_IPX Socket Options</a>



<a href="/windows/desktop/WinSock/sol-appletalk-socket-options">SOL_APPLETALK Socket Options</a>



<a href="/windows/desktop/WinSock/sol-irlmp-socket-options">SOL_IRLMP Socket Options</a>



<a href="/windows/desktop/WinSock/sol-socket-socket-options">SOL_SOCKET Socket Options</a>



<a href="/windows/desktop/WinSock/socket-options">Socket Options</a>



<a href="/windows/desktop/api/winsock/nf-winsock-wsaasyncselect">WSAAsyncSelect</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaconnect">WSAConnect</a>



<a href="/windows/desktop/api/winsock/nf-winsock-wsagetlasterror">WSAGetLastError</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaioctl">WSAIoctl</a>



<a href="/windows/desktop/api/winsock/nf-winsock-wsasetlasterror">WSASetLastError</a>



<a href="/windows/desktop/WinSock/winsock-functions">Winsock Functions</a>



<a href="/windows/desktop/api/winsock/nf-winsock-ioctlsocket">ioctlsocket</a>



<a href="/windows/desktop/api/winsock/nf-winsock-recv">recv</a>



<a href="/windows/desktop/api/winsock/nf-winsock-setsockopt">setsockopt</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-socket">socket</a>
