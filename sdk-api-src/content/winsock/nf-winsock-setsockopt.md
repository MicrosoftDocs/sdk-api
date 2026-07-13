---
UID: NF:winsock.setsockopt
title: setsockopt function (winsock.h)
description: The setsockopt function (winsock.h) sets a socket option.
helpviewer_keywords: ["_win32_setsockopt_2","setsockopt","setsockopt function [Winsock]","winsock.setsockopt_2","winsock/setsockopt"]
old-location: winsock\setsockopt_2.htm
tech.root: WinSock
ms.assetid: 3a6960c9-0c04-4403-aee1-ce250459dc30
ms.date: 08/16/2022
ms.keywords: _win32_setsockopt_2, setsockopt, setsockopt function [Winsock], winsock.setsockopt_2, winsock/setsockopt
req.header: winsock.h
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
 - setsockopt
 - winsock/setsockopt
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
 - setsockopt
---

## -description

The <b>setsockopt</b> function sets a socket option.

## -parameters

### -param s [in]

A descriptor that identifies a socket.

### -param level [in]

The level at which the option is defined (for example, SOL_SOCKET).

### -param optname [in]

The socket option for which the value is to be set (for example, SO_BROADCAST). The <i>optname</i> parameter must be a socket option defined within the specified <i>level</i>, or behavior is undefined.

### -param optval [in]

A pointer to the buffer in which the value for the requested option is specified.

### -param optlen [in]

The size, in bytes, of the buffer pointed to by the <i>optval</i> parameter.

## -returns

If no error occurs, 
<b>setsockopt</b> returns zero. Otherwise, a value of SOCKET_ERROR is returned, and a specific error code can be retrieved by calling 
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
The network subsystem has failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEFAULT</a></b></dt>
</dl>
</td>
<td width="60%">
The buffer pointed to by the <i>optval</i> parameter is not in a valid part of the process address space or the  <i>optlen</i> parameter is too small.

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
The <i>level</i> parameter is not valid, or the information in the buffer pointed to by the <i>optval</i> parameter is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAENETRESET</a></b></dt>
</dl>
</td>
<td width="60%">
The connection has timed out when <a href="/windows/desktop/WinSock/so-keepalive">SO_KEEPALIVE</a> is set.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAENOPROTOOPT</a></b></dt>
</dl>
</td>
<td width="60%">
The option is unknown or unsupported for the specified provider or socket (see SO_GROUP_PRIORITY limitations).

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAENOTCONN</a></b></dt>
</dl>
</td>
<td width="60%">
The connection has been reset when <a href="/windows/desktop/WinSock/so-keepalive">SO_KEEPALIVE</a> is set.

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
<b>setsockopt</b> function sets the current value for a socket option associated with a socket of any type, in any state. Although options can exist at multiple protocol levels, they are always present at the uppermost socket level. Options affect socket operations, such as whether expedited data (OOB data for example) is received in the normal data stream, and whether broadcast messages can be sent on the socket.

<div class="alert"><b>Note</b>  If the 
<b>setsockopt</b> function is called before the 
<a href="/windows/desktop/api/winsock/nf-winsock-bind">bind</a> function, TCP/IP options will not be checked by using TCP/IP until the 
<b>bind</b> occurs. In this case, the 
<b>setsockopt</b> function call will always succeed, but the 
<b>bind</b> function call can fail because of an early 
<b>setsockopt</b> call failing.</div>
<div> </div>
<div class="alert"><b>Note</b>  If a socket is opened, a 
<b>setsockopt</b> call is made, and then a 
<a href="/windows/desktop/api/winsock/nf-winsock-sendto">sendto</a> call is made, Windows Sockets performs an implicit 
<a href="/windows/desktop/api/winsock/nf-winsock-bind">bind</a> function call.</div>
<div> </div>
There are two types of socket options: Boolean options that enable or disable a feature or behavior, and options that require an integer value or structure. To enable a Boolean option, the <i>optval</i> parameter points to a nonzero integer. To disable the option <i>optval</i> points to an integer equal to zero. The <i>optlen</i> parameter should be equal to <code>sizeof(int)</code> for Boolean options. For other options, <i>optval</i> points to an integer or structure that contains the desired value for the option, and <i>optlen</i> is the length of the integer or structure.

The following tables list some of the common options supported by the <b>setsockopt</b> function. The Type column identifies the type of data addressed by <i>optval</i> parameter. The  Description column provides some basic information about the socket option. For more complete lists of socket options and more detailed information (default values, for example), see the detailed topics under <a href="/windows/desktop/WinSock/socket-options">Socket Options</a>. 

<i>level</i> = <b>SOL_SOCKET</b>

<table>
<tr>
<th>Value</th>
<th>Type</th>
<th>Description</th>
</tr>
<tr>
<td>SO_BROADCAST</td>
<td>BOOL</td>
<td>Configures a socket for sending broadcast data.</td>
</tr>
<tr>
<td>SO_CONDITIONAL_ACCEPT</td>
<td>BOOL</td>
<td>Enables incoming connections are to be accepted or rejected by the application, not by the protocol stack.</td>
</tr>
<tr>
<td>SO_DEBUG</td>
<td>BOOL</td>
<td>Enables debug output. Microsoft providers currently do not output any debug information.</td>
</tr>
<tr>
<td>SO_DONTLINGER</td>
<td>BOOL</td>
<td>Does not block close waiting for unsent data to be sent. Setting this option is equivalent to setting SO_LINGER with <b>l_onoff</b> set to zero.</td>
</tr>
<tr>
<td>SO_DONTROUTE</td>
<td>BOOL</td>
<td>Sets whether outgoing data should be sent on interface the socket is bound to and not a routed on some other interface. This option is not supported on ATM sockets (results in an error).</td>
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
<td>Enables sending keep-alive packets for a socket connection. Not supported on ATM sockets (results in an error).</td>
</tr>
<tr>
<td>SO_LINGER</td>
<td>
<a href="/windows/desktop/api/winsock/ns-winsock-linger">LINGER</a>
</td>
<td>Lingers on close if unsent data is present.</td>
</tr>
<tr>
<td>SO_OOBINLINE</td>
<td>BOOL</td>
<td>Indicates that out-of-bound data should be returned in-line with regular data. This option is only valid for connection-oriented protocols that support out-of-band data. For a discussion of this topic, see 
<a href="/windows/desktop/WinSock/protocol-independent-out-of-band-data-2">Protocol Independent Out-Of-band Data</a>.</td>
</tr>
<tr>
<td>SO_RCVBUF</td>
<td>int</td>
<td>Specifies the total per-socket buffer space reserved for receives. </td>
</tr>
<tr>
<td>SO_REUSEADDR</td>
<td>BOOL</td>
<td>Allows the socket to be bound to an address that is already in use. For more information, see 
<a href="/windows/desktop/api/winsock/nf-winsock-bind">bind</a>. Not applicable on ATM sockets.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/WinSock/so-exclusiveaddruse">SO_EXCLUSIVEADDRUSE</a>
</td>
<td>BOOL</td>
<td>Enables a socket to be bound for exclusive access. Does not require administrative privilege. </td>
</tr>
<tr>
<td>SO_RCVTIMEO</td>
<td>DWORD</td>
<td>Sets the timeout, in milliseconds, for blocking receive calls. </td>
</tr>
<tr>
<td>SO_SNDBUF</td>
<td>int</td>
<td>Specifies the total per-socket buffer space reserved for sends.</td>
</tr>
<tr>
<td>SO_SNDTIMEO</td>
<td>DWORD</td>
<td>The timeout, in milliseconds, for blocking send calls. </td>
</tr>
<tr>
<td>SO_UPDATE_ACCEPT_CONTEXT</td>
<td>UINT_PTR</td>
<td>Updates the accepting socket with the context of the listening socket.</td>
</tr>
<tr>
<td>PVD_CONFIG</td>
<td>Service Provider Dependent</td>
<td>This object stores the configuration information for the service provider associated with socket <i>s</i>. The exact format of this data structure is service provider specific.</td>
</tr>
</table>
 
For more complete and detailed information about socket options for <i>level</i> = <b>SOL_SOCKET</b>, see <a href="/windows/desktop/WinSock/sol-socket-socket-options">SOL_SOCKET Socket Options</a>.

<i>level</i> = <b>IPPROTO_TCP</b>

See **TCP_NODELAY** in [IPPROTO_TCP socket options](/windows/desktop/WinSock/ipproto-tcp-socket-options). Also see that topic for more complete and detailed information about socket options for <i>level</i> = <b>IPPROTO_TCP</b>.

<i>level</i> = <b>NSPROTO_IPX</b>

<table>
<tr>
<th>Value</th>
<th>Type</th>
<th>Description</th>
</tr>
<tr>
<td>IPX_PTYPE</td>
<td>int</td>
<td>Sets the IPX packet type.</td>
</tr>
<tr>
<td>IPX_FILTERPTYPE</td>
<td>int</td>
<td>Sets the receive filter packet type</td>
</tr>
<tr>
<td>IPX_STOPFILTERPTYPE</td>
<td>int</td>
<td>Stops filtering the filter type set with IPX_FILTERTYPE</td>
</tr>
<tr>
<td>IPX_DSTYPE</td>
<td>int</td>
<td>Sets the value of the data stream field in the SPX header on every packet sent.</td>
</tr>
<tr>
<td>IPX_EXTENDED_ADDRESS</td>
<td>BOOL</td>
<td>Sets whether extended addressing is enabled.</td>
</tr>
<tr>
<td>IPX_RECVHDR</td>
<td>BOOL</td>
<td>Sets whether the protocol header is sent up on all receive headers.</td>
</tr>
<tr>
<td>IPX_RECEIVE_BROADCAST</td>
<td>BOOL</td>
<td>Indicates broadcast packets are likely on the socket. Set to <b>TRUE</b> by default. Applications that do not use broadcasts should set this to <b>FALSE</b> for better system performance.</td>
</tr>
<tr>
<td>IPX_IMMEDIATESPXACK</td>
<td>BOOL</td>
<td>Directs SPX connections not to delay before sending an ACK. Applications without back-and-forth traffic should set this to <b>TRUE</b> to increase performance.</td>
</tr>
</table>
 

For more complete and detailed information about socket options for <i>level</i> = <b>NSPROTO_IPX</b>, see <a href="/windows/desktop/WinSock/nsproto-ipx-socket-options">NSPROTO_IPX Socket Options</a>.

BSD options not supported for 
<b>setsockopt</b> are shown in the following table.

<table>
<tr>
<th>Value</th>
<th>Type</th>
<th>Description</th>
</tr>
<tr>
<td>SO_ACCEPTCONN</td>
<td>BOOL</td>
<td>Returns whether a socket is in listening mode. This option is only Valid for connection-oriented protocols. This socket option is not supported for the setting.</td>
</tr>
<tr>
<td>SO_RCVLOWAT</td>
<td>int</td>
<td>A socket option from BSD UNIX included for backward compatibility. This option sets the minimum number of bytes to process for socket input operations. 
</td>
</tr>
<tr>
<td>SO_SNDLOWAT</td>
<td>int</td>
<td>A socket option from BSD UNIX included for backward compatibility. This option sets the minimum number of bytes to process for socket output operations. </td>
</tr>
<tr>
<td>SO_TYPE</td>
<td>int</td>
<td>Returns the socket type for the given socket (SOCK_STREAM or SOCK_DGRAM, for example This socket option is not supported for the setting the socket type.</td>
</tr>
</table>
 



<div class="alert"><b>Note</b>  When issuing a blocking Winsock call such as <b>setsockopt</b>, Winsock may need to wait for a network event before the call can complete. Winsock performs an alertable wait in this situation, which can be interrupted by an asynchronous procedure call (APC) scheduled on the same thread. Issuing another blocking Winsock call inside an APC that interrupted an ongoing blocking Winsock call on the same thread will lead to undefined behavior, and must never be attempted by Winsock clients. </div>
<div> </div>
<h3><a id="Example_Code"></a><a id="example_code"></a><a id="EXAMPLE_CODE"></a>Example Code</h3>
The following example demonstrates the <b>setsockopt</b> function.


```cpp
#ifndef UNICODE
#define UNICODE
#endif

#ifndef WIN32_LEAN_AND_MEAN
#define WIN32_LEAN_AND_MEAN
#endif

#include <winsock2.h>
#include <Ws2tcpip.h>
#include <stdio.h>

// Link with ws2_32.lib
#pragma comment(lib, "Ws2_32.lib")

int main()
{

    //---------------------------------------
    // Declare variables
    WSADATA wsaData;

    SOCKET ListenSocket;
    sockaddr_in service;

    int iResult = 0;

    BOOL bOptVal = FALSE;
    int bOptLen = sizeof (BOOL);

    int iOptVal = 0;
    int iOptLen = sizeof (int);

    //---------------------------------------
    // Initialize Winsock
    iResult = WSAStartup(MAKEWORD(2, 2), &wsaData);
    if (iResult != NO_ERROR) {
        wprintf(L"Error at WSAStartup()\n");
        return 1;
    }
    //---------------------------------------
    // Create a listening socket
    ListenSocket = socket(AF_INET, SOCK_STREAM, IPPROTO_TCP);
    if (ListenSocket == INVALID_SOCKET) {
        wprintf(L"socket function failed with error: %u\n", WSAGetLastError());
        WSACleanup();
        return 1;
    }
    //---------------------------------------
    // Bind the socket to the local IP address
    // and port 27015
    hostent *thisHost;
    char *ip;
    u_short port;
    port = 27015;
    thisHost = gethostbyname("");
    ip = inet_ntoa(*(struct in_addr *) *thisHost->h_addr_list);

    service.sin_family = AF_INET;
    service.sin_addr.s_addr = inet_addr(ip);
    service.sin_port = htons(port);

    iResult = bind(ListenSocket, (SOCKADDR *) & service, sizeof (service));
    if (iResult == SOCKET_ERROR) {
        wprintf(L"bind failed with error %u\n", WSAGetLastError());
        closesocket(ListenSocket);
        WSACleanup();
        return 1;
    }
    //---------------------------------------
    // Initialize variables and call setsockopt. 
    // The SO_KEEPALIVE parameter is a socket option 
    // that makes the socket send keepalive messages
    // on the session. The SO_KEEPALIVE socket option
    // requires a boolean value to be passed to the
    // setsockopt function. If TRUE, the socket is
    // configured to send keepalive messages, if FALSE
    // the socket configured to NOT send keepalive messages.
    // This section of code tests the setsockopt function
    // by checking the status of SO_KEEPALIVE on the socket
    // using the getsockopt function.

    bOptVal = TRUE;

    iResult = getsockopt(ListenSocket, SOL_SOCKET, SO_KEEPALIVE, (char *) &iOptVal, &iOptLen);
    if (iResult == SOCKET_ERROR) {
        wprintf(L"getsockopt for SO_KEEPALIVE failed with error: %u\n", WSAGetLastError());
    } else
        wprintf(L"SO_KEEPALIVE Value: %ld\n", iOptVal);

    iResult = setsockopt(ListenSocket, SOL_SOCKET, SO_KEEPALIVE, (char *) &bOptVal, bOptLen);
    if (iResult == SOCKET_ERROR) {
        wprintf(L"setsockopt for SO_KEEPALIVE failed with error: %u\n", WSAGetLastError());
    } else
        wprintf(L"Set SO_KEEPALIVE: ON\n");

    iResult = getsockopt(ListenSocket, SOL_SOCKET, SO_KEEPALIVE, (char *) &iOptVal, &iOptLen);
    if (iResult == SOCKET_ERROR) {
        wprintf(L"getsockopt for SO_KEEPALIVE failed with error: %u\n", WSAGetLastError());
    } else
        wprintf(L"SO_KEEPALIVE Value: %ld\n", iOptVal);

    closesocket(ListenSocket);
    WSACleanup();
    return 0;
}


```


<h3><a id="Notes_for_IrDA_Sockets"></a><a id="notes_for_irda_sockets"></a><a id="NOTES_FOR_IRDA_SOCKETS"></a>Notes for IrDA Sockets</h3>

When developing applications using Windows sockets for IrDA, note the following:

<ul>
<li>The Af_irda.h header file must be explicitly included.</li>
<li>IrDA provides the following socket option:<table>
<tr>
<th>Value</th>
<th>Type</th>
<th>Meaning</th>
</tr>
<tr>
<td>IRLMP_IAS_SET</td>
<td>*IAS_SET</td>
<td>Sets IAS attributes</td>
</tr>
</table>
 

</li>
</ul>


The IRLMP_IAS_SET socket option enables the application to set a single attribute of a single class in the local IAS. The application specifies the class to set, the attribute, and attribute type. The application is expected to allocate a buffer of the necessary size for the passed parameters.

IrDA provides an IAS database that stores IrDA-based information. Limited access to the IAS database is available through the Windows Sockets 2 interface, but such access is not normally used by applications, and exists primarily to support connections to non-Windows devices that are not compliant with the Windows Sockets 2 IrDA conventions.

The following structure, <b>IAS_SET</b>, is used with the IRLMP_IAS_SET setsockopt option to manage the local IAS database:


```cpp

// #include <Af_irda.h> for this struct

typedef struct _IAS_SET {
    u_char      irdaClassName[IAS_MAX_CLASSNAME];
    char      irdaAttribName[IAS_MAX_ATTRIBNAME];
    u_long    irdaAttribType;
    union
    {
              LONG irdaAttribInt;
              struct
              {
                   u_long   Len;
                   u_char    OctetSeq[IAS_MAX_OCTET_STRING];
              } irdaAttribOctetSeq;
              struct
              {
                   u_long    Len;
                   u_long    CharSet;
                   u_char    UsrStr[IAS_MAX_USER_STRING];
              } irdaAttribUsrStr;
    } irdaAttribute;
} IAS_SET, *PIAS_SET, FAR *LPIASSET;

```


The following structure, <b>IAS_QUERY</b>, is used with the IRLMP_IAS_QUERY setsockopt option to query a peer's IAS database:


```cpp

// #include <Af_irda.h> for this struct

typedef struct _WINDOWS_IAS_QUERY {
        u_char   irdaDeviceID[4];
        char     irdaClassName[IAS_MAX_CLASSNAME];
        char     irdaAttribName[IAS_MAX_ATTRIBNAME];
        u_long   irdaAttribType;
        union
        {
                  LONG    irdaAttribInt;
                  struct
                  {
                          u_long  Len;
                          u_char  OctetSeq[IAS_MAX_OCTET_STRING];
                  } irdaAttribOctetSeq;
                  struct
                  {
                          u_long  Len;
                          u_long  CharSet;
                          u_char  UsrStr[IAS_MAX_USER_STRING];
                  } irdaAttribUsrStr;
        } irdaAttribute;
} IAS_QUERY, *PIAS_QUERY, FAR *LPIASQUERY;

```


Many SO_ level socket options are not meaningful to IrDA. Only SO_LINGER is specifically supported.

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



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaeventselect">WSAEventSelect</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaioctl">WSAIoctl</a>



<a href="/windows/desktop/WinSock/winsock-functions">Winsock Functions</a>



<a href="/windows/desktop/api/winsock/nf-winsock-bind">bind</a>



<a href="/windows/desktop/api/winsock/nf-winsock-getsockopt">getsockopt</a>



<a href="/windows/desktop/api/winsock/nf-winsock-ioctlsocket">ioctlsocket</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-socket">socket</a>
