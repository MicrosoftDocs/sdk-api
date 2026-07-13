---
UID: NF:winsock.AcceptEx
title: AcceptEx function (winsock.h)
description: The AcceptEx function (winsock.h) accepts a new connection, returns the local and remote address, and receives the first block of data sent by the client application. 
helpviewer_keywords: ["AcceptEx","AcceptEx function [Winsock]","_win32_acceptex_2","winsock.acceptex_2","winsock/AcceptEx"]
old-location: winsock\acceptex_2.htm
tech.root: WinSock
ms.assetid: cfd4c169-a8af-46cc-9b0e-fd7fb5aad61b
ms.date: 08/15/2022
ms.keywords: AcceptEx, AcceptEx function [Winsock], _win32_acceptex_2, winsock.acceptex_2, winsock/AcceptEx
req.header: winsock.h
req.include-header: Mswsock.h
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
req.lib: Mswsock.lib
req.dll: Mswsock.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - AcceptEx
 - winsock/AcceptEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Mswsock.dll
api_name:
 - AcceptEx
---

# AcceptEx function


## -description

The 
<b>AcceptEx</b> function accepts a new connection, returns the local and remote address, and receives the first block of data sent by the client application. <div class="alert"><b>Note</b>  This function is a Microsoft-specific extension to the Windows Sockets specification.</div>
<div> </div>

## -parameters

### -param sListenSocket [in]

A descriptor identifying a socket that has already been called with the 
<a href="/windows/desktop/api/winsock2/nf-winsock2-listen">listen</a> function. A server application waits for attempts to connect on this socket.

### -param sAcceptSocket [in]

A descriptor identifying a socket on which to accept an incoming connection. This socket must not be bound or connected.

### -param lpOutputBuffer [in]

A pointer to a buffer that receives the first block of data sent on a new connection, the local address of the server, and the remote address of the client. The receive data is written to the first part of the buffer starting at offset zero, while the addresses are written to the latter part of the buffer. This parameter must be specified.

### -param dwReceiveDataLength [in]

The number of bytes in <i>lpOutputBuffer</i> that will be used for actual receive data at the beginning of the buffer. This size should not include the size of the local address of the server, nor the remote address of the client; they are appended to the output buffer. If <i>dwReceiveDataLength</i> is zero, accepting the connection will not result in a receive operation. Instead, 
<b>AcceptEx</b> completes as soon as a connection arrives, without waiting for any data.

### -param dwLocalAddressLength [in]

The number of bytes reserved for the local address information. This value must be at least 16 bytes more than the maximum address length for the transport protocol in use.

### -param dwRemoteAddressLength [in]

The number of bytes reserved for the remote address information. This value must be at least 16 bytes more than the maximum address length for the transport protocol in use. Cannot be zero.

### -param lpdwBytesReceived [out]

A pointer to a <b>DWORD</b> that receives the count of bytes received. This parameter is set only if the operation completes synchronously. If it returns ERROR_IO_PENDING and is completed later, then this <b>DWORD</b> is never set and you must obtain the number of bytes read from the completion notification mechanism.

### -param lpOverlapped [in]

An 
<a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure that is used to process the request. This parameter must be specified; it cannot be <b>NULL</b>.

## -returns

If no error occurs, the 
<b>AcceptEx</b> function completed successfully and a value of <b>TRUE</b> is returned.

If the function fails, 
<b>AcceptEx</b> returns <b>FALSE</b>. The 
<a href="/windows/desktop/api/winsock/nf-winsock-wsagetlasterror">WSAGetLastError</a> function can then be called to return extended error information. If 
<b>WSAGetLastError</b> returns <b>ERROR_IO_PENDING</b>, then the operation was successfully initiated and is still in progress. If the error is WSAECONNRESET, an incoming connection was indicated, but was subsequently terminated by the remote peer prior to accepting the call.

## -remarks

The 
<b>AcceptEx</b> function combines several socket functions into a single API/kernel transition. The 
<b>AcceptEx</b> function, when successful, performs three tasks:

<ul>
<li>A new connection is accepted.</li>
<li>Both the local and remote addresses for the connection are returned.</li>
<li>The first block of data sent by the remote is received.</li>
</ul>



<div class="alert"><b>Note</b>  The function pointer for the 
<b>AcceptEx</b> function must be obtained at run time by making a call to the 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaioctl">WSAIoctl</a> function with the <b>SIO_GET_EXTENSION_FUNCTION_POINTER</b> opcode specified. The input buffer passed to the <b>WSAIoctl</b> function must contain <b>WSAID_ACCEPTEX</b>, a globally unique identifier (GUID) whose value identifies the <b>AcceptEx</b> extension function. On success, the output returned by the <b>WSAIoctl</b> function contains a pointer to the <b>AcceptEx</b> function. The <b>WSAID_ACCEPTEX</b> GUID is defined in the <i>Mswsock.h</i> header file.</div>
<div> </div>


A program can make a connection to a socket more quickly using 
<b>AcceptEx</b> instead of the 
<a href="/windows/desktop/api/winsock2/nf-winsock2-accept">accept</a> function.

A single output buffer receives the data, the local socket address (the server), and the remote socket address (the client).

Using a single buffer improves performance. When using 
<b>AcceptEx</b>, the 
<a href="/windows/desktop/api/mswsock/nf-mswsock-getacceptexsockaddrs">GetAcceptExSockaddrs</a> function must be called to parse the buffer into its three distinct parts (data, local socket address, and remote socket address). On Windows XP and later, once the 
<b>AcceptEx</b> function completes and the <b>SO_UPDATE_ACCEPT_CONTEXT</b> option is set on the accepted socket, the local address associated with the accepted socket can also be retrieved using the 
<a href="/windows/desktop/api/winsock/nf-winsock-getsockname">getsockname</a> function. Likewise, the remote address associated with the accepted socket can be retrieved using the 
<a href="/windows/desktop/api/winsock/nf-winsock-getpeername">getpeername</a> function.

The buffer size for the local and remote address must be 16 bytes more than the size of the 
<a href="/windows/desktop/WinSock/sockaddr-2">sockaddr</a> structure for the transport protocol in use because the addresses are written in an internal format. For example, the size of a <b>sockaddr_in</b> (the address structure for TCP/IP) is 16 bytes. Therefore, a buffer size of at least 32 bytes must be specified for the local and remote addresses.

The 
<b>AcceptEx</b> function uses overlapped I/O, unlike the 
<a href="/windows/desktop/api/winsock2/nf-winsock2-accept">accept</a> function. If your application uses 
<b>AcceptEx</b>, it can service a large number of clients with a relatively small number of threads. As with all overlapped Windows functions, either Windows events or completion ports can be used as a completion notification mechanism.


Another key difference between the 
<b>AcceptEx</b> function and the 
<a href="/windows/desktop/api/winsock2/nf-winsock2-accept">accept</a> function is that 
<b>AcceptEx</b> requires the caller to already have two sockets:

<ul>
<li>One that specifies the socket on which to listen.</li>
<li>One that specifies the socket on which to accept the connection.</li>
</ul>


The <i>sAcceptSocket</i> parameter must be an open socket that is neither bound nor connected.

The <i>lpNumberOfBytesTransferred</i> parameter of the 
<a href="/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus">GetQueuedCompletionStatus</a> function or the 
<a href="/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult">GetOverlappedResult</a> function indicates the number of bytes received in the request.


When this operation is successfully completed, <i>sAcceptSocket</i> can be passed, but to the following functions only:

<dl>
<dd>
<a href="/windows/desktop/api/fileapi/nf-fileapi-readfile">ReadFile</a>
</dd>
<dd>
<a href="/windows/desktop/api/fileapi/nf-fileapi-writefile">WriteFile</a>
</dd>
<dd>
<a href="/windows/desktop/api/winsock2/nf-winsock2-send">send</a>
</dd>
<dd>
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsasend">WSASend</a>
</dd>
<dd>
<a href="/windows/desktop/api/winsock/nf-winsock-recv">recv</a>
</dd>
<dd>
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsarecv">WSARecv</a>
</dd>
<dd>
<a href="/windows/desktop/api/mswsock/nf-mswsock-transmitfile">TransmitFile</a>
</dd>
<dd>
<a href="/windows/desktop/api/winsock/nf-winsock-closesocket">closesocket</a>
</dd>
<dd>
<a href="/windows/desktop/api/winsock/nf-winsock-setsockopt">setsockopt</a>(only for SO_UPDATE_ACCEPT_CONTEXT)</dd>
</dl>
<div class="alert"><b>Note</b>  If the 
<a href="/windows/desktop/api/mswsock/nf-mswsock-transmitfile">TransmitFile</a> function is called with both the TF_DISCONNECT and TF_REUSE_SOCKET flags, the specified socket has been returned to a state in which it is neither bound nor connected. The socket handle can then be passed to the 
<b>AcceptEx</b> function in the <i>sAcceptSocket</i> parameter, but the socket cannot be passed to the <a href="/windows/desktop/api/mswsock/nc-mswsock-lpfn_connectex">ConnectEx</a> function.</div>
<div> </div>


When the 
<b>AcceptEx</b> function returns, the socket <i>sAcceptSocket</i> is in the default state for a connected socket. The socket <i>sAcceptSocket</i> does not inherit the properties of the socket associated with <i>sListenSocket</i> parameter until SO_UPDATE_ACCEPT_CONTEXT is set on the socket. Use the 
<a href="/windows/desktop/api/winsock/nf-winsock-setsockopt">setsockopt</a> function to set the SO_UPDATE_ACCEPT_CONTEXT option, specifying <i>sAcceptSocket</i> as the socket handle and <i>sListenSocket</i> as the option value.

For example:


```cpp
//Need to #include <mswsock.h> for SO_UPDATE_ACCEPT_CONTEXT

int iResult = 0;

iResult =  setsockopt( sAcceptSocket, SOL_SOCKET, SO_UPDATE_ACCEPT_CONTEXT, 
    (char *)&sListenSocket, sizeof(sListenSocket) );
   

```


If a receive buffer is provided, the overlapped operation will not complete until a connection is accepted and data is read. Use the 
<a href="/windows/desktop/api/winsock/nf-winsock-getsockopt">getsockopt</a> function with the SO_CONNECT_TIME option to check whether a connection has been accepted. If it has been accepted, you can determine how long the connection has been established. The return value is the number of seconds that the socket has been connected. If the socket is not connected, the 
<b>getsockopt</b> returns 0xFFFFFFFF. Applications that check whether the overlapped operation has completed, in combination with the SO_CONNECT_TIME option, can determine that a connection has been accepted but no data has been received. Scrutinizing a connection in this manner enables an application to determine whether connections that have been established for a while have received no data. It is recommended such connections be terminated by closing the accepted socket, which forces the 
<b>AcceptEx</b> function call to complete with an error.

For example:


```cpp

INT seconds;
INT bytes = sizeof(seconds);
int iResult = 0;

iResult = getsockopt( sAcceptSocket, SOL_SOCKET, SO_CONNECT_TIME,
                      (char *)&seconds, (PINT)&bytes );

if ( iResult != NO_ERROR ) {
    printf( "getsockopt(SO_CONNECT_TIME) failed: %u\n", WSAGetLastError( ) );
    exit(1);
}

```



<div class="alert"><b>Note</b>   All I/O initiated by a given thread is canceled when that thread exits. For overlapped sockets, pending asynchronous operations can fail if the thread is closed before the  operations complete. See <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-exitthread">ExitThread</a> for more information.</div>
<div> </div>


<b>Windows Phone 8:</b> This function is supported for Windows Phone Store apps on Windows Phone 8 and later.

<b>Windows 8.1</b> and <b>Windows Server 2012 R2</b>: This function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and later.

<h3><a id="Example_Code"></a><a id="example_code"></a><a id="EXAMPLE_CODE"></a>Example Code</h3>
The following example uses the <b>AcceptEx</b> function using overlapped I/O and completion ports.


```cpp
#ifndef UNICODE
#define UNICODE
#endif

#define WIN32_LEAN_AND_MEAN

#include <winsock2.h>
#include <ws2tcpip.h>
#include <mswsock.h>
#include <stdio.h>

// Need to link with Ws2_32.lib
#pragma comment(lib, "Ws2_32.lib")

int main()
{
    //----------------------------------------
    // Declare and initialize variables
    WSADATA wsaData;
    int iResult = 0;
    BOOL bRetVal = FALSE;

    HANDLE hCompPort;
    HANDLE hCompPort2;
    
    LPFN_ACCEPTEX lpfnAcceptEx = NULL;
    GUID GuidAcceptEx = WSAID_ACCEPTEX;
    WSAOVERLAPPED olOverlap;

    SOCKET ListenSocket = INVALID_SOCKET;
    SOCKET AcceptSocket = INVALID_SOCKET;
    sockaddr_in service;
    char lpOutputBuf[1024];
    int outBufLen = 1024;
    DWORD dwBytes;

    hostent *thisHost;
    char *ip;
    u_short port;

    // Initialize Winsock
    iResult = WSAStartup(MAKEWORD(2, 2), &wsaData);
    if (iResult != NO_ERROR) {
        wprintf(L"Error at WSAStartup\n");
        return 1;
    }    

    // Create a handle for the completion port
    hCompPort = CreateIoCompletionPort(INVALID_HANDLE_VALUE, NULL, (u_long) 0, 0);
    if (hCompPort == NULL) {
        wprintf(L"CreateIoCompletionPort failed with error: %u\n",
            GetLastError() );
        WSACleanup();
        return 1;
    }
            
    // Create a listening socket
    ListenSocket = socket(AF_INET, SOCK_STREAM, IPPROTO_TCP);
    if (ListenSocket == INVALID_SOCKET) {
        wprintf(L"Create of ListenSocket socket failed with error: %u\n",
            WSAGetLastError() );
        WSACleanup();
        return 1;
    }

    // Associate the listening socket with the completion port
    CreateIoCompletionPort((HANDLE) ListenSocket, hCompPort, (u_long) 0, 0);

    //----------------------------------------
    // Bind the listening socket to the local IP address
    // and port 27015
    port = 27015;
    thisHost = gethostbyname("");
    ip = inet_ntoa(*(struct in_addr *) *thisHost->h_addr_list);

    service.sin_family = AF_INET;
    service.sin_addr.s_addr = inet_addr(ip);
    service.sin_port = htons(port);

    if (bind(ListenSocket, (SOCKADDR *) & service, sizeof (service)) == SOCKET_ERROR) {
        wprintf(L"bind failed with error: %u\n", WSAGetLastError());
        closesocket(ListenSocket);
        WSACleanup();
        return 1;
    }

    //----------------------------------------
    // Start listening on the listening socket
    iResult = listen(ListenSocket, 100);
    if (iResult == SOCKET_ERROR) {
        wprintf(L"listen failed with error: %u\n", WSAGetLastError());
        closesocket(ListenSocket);
        WSACleanup();
        return 1;
    }

    wprintf(L"Listening on address: %s:%d\n", ip, port);

    // Load the AcceptEx function into memory using WSAIoctl.
    // The WSAIoctl function is an extension of the ioctlsocket()
    // function that can use overlapped I/O. The function's 3rd
    // through 6th parameters are input and output buffers where
    // we pass the pointer to our AcceptEx function. This is used
    // so that we can call the AcceptEx function directly, rather
    // than refer to the Mswsock.lib library.
    iResult = WSAIoctl(ListenSocket, SIO_GET_EXTENSION_FUNCTION_POINTER,
             &GuidAcceptEx, sizeof (GuidAcceptEx), 
             &lpfnAcceptEx, sizeof (lpfnAcceptEx), 
             &dwBytes, NULL, NULL);
    if (iResult == SOCKET_ERROR) {
        wprintf(L"WSAIoctl failed with error: %u\n", WSAGetLastError());
        closesocket(ListenSocket);
        WSACleanup();
        return 1;
    }

    // Create an accepting socket
    AcceptSocket = socket(AF_INET, SOCK_STREAM, IPPROTO_TCP);
    if (AcceptSocket == INVALID_SOCKET) {
        wprintf(L"Create accept socket failed with error: %u\n", WSAGetLastError());
        closesocket(ListenSocket);
        WSACleanup();
        return 1;
    }

    // Empty our overlapped structure and accept connections.
    memset(&olOverlap, 0, sizeof (olOverlap));

    bRetVal = lpfnAcceptEx(ListenSocket, AcceptSocket, lpOutputBuf,
                 outBufLen - ((sizeof (sockaddr_in) + 16) * 2),
                 sizeof (sockaddr_in) + 16, sizeof (sockaddr_in) + 16, 
                 &dwBytes, &olOverlap);
    if (bRetVal == FALSE) {
        wprintf(L"AcceptEx failed with error: %u\n", WSAGetLastError());
        closesocket(AcceptSocket);
        closesocket(ListenSocket);
        WSACleanup();
        return 1;
    }

    // Associate the accept socket with the completion port
    hCompPort2 = CreateIoCompletionPort((HANDLE) AcceptSocket, hCompPort, (u_long) 0, 0); 
    // hCompPort2 should be hCompPort if this succeeds
    if (hCompPort2 == NULL) {
        wprintf(L"CreateIoCompletionPort associate failed with error: %u\n",
            GetLastError() );
        closesocket(AcceptSocket);
        closesocket(ListenSocket);
        WSACleanup();
        return 1;
    }
    
    // Continue on to use send, recv, TransmitFile(), etc.,.
    //...

    return 0;
}


```


<h3><a id="Notes_for_QoS"></a><a id="notes_for_qos"></a><a id="NOTES_FOR_QOS"></a>Notes for QoS</h3>
The 
<a href="/windows/desktop/api/mswsock/nf-mswsock-transmitfile">TransmitFile</a> function allows the setting of two flags, TF_DISCONNECT or TF_REUSE_SOCKET, that return the socket to a "disconnected, reusable" state after the file has been transmitted. These flags should not be used on a socket where quality of service has been requested, since the service provider may immediately delete any quality of service associated with the socket before the file transfer has completed. The best approach for a QoS-enabled socket is to simply call the 
<a href="/windows/desktop/api/winsock/nf-winsock-closesocket">closesocket</a> function when the file transfer has completed, rather than relying on these flags.

<h3><a id="Notes_for_ATM"></a><a id="notes_for_atm"></a><a id="NOTES_FOR_ATM"></a>Notes for ATM</h3>
There are important issues associated with connection setup when using Asynchronous Transfer Mode (ATM) with Windows Sockets 2. Please see the Remarks section in the 
<a href="/windows/desktop/api/winsock2/nf-winsock2-accept">accept</a> function documentation for important ATM connection setup information.

## -see-also

<a href="/windows/desktop/api/mswsock/nf-mswsock-getacceptexsockaddrs">GetAcceptExSockaddrs</a>



<a href="/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult">GetOverlappedResult</a>



<a href="/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus">GetQueuedCompletionStatus</a>



<a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a>



<a href="/windows/desktop/api/mswsock/nf-mswsock-transmitfile">TransmitFile</a>



<a href="/windows/desktop/WinSock/winsock-functions">Winsock Functions</a>



<a href="/windows/desktop/WinSock/winsock-reference">Winsock Reference</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-accept">accept</a>



<a href="/windows/desktop/api/winsock/nf-winsock-closesocket">closesocket</a>



<a href="/windows/desktop/api/winsock/nf-winsock-getsockopt">getsockopt</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-listen">listen</a>



<a href="/windows/desktop/WinSock/sockaddr-2">sockaddr</a>
