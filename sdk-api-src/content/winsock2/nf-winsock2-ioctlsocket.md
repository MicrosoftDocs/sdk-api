---
UID: NF:winsock2.ioctlsocket
title: ioctlsocket function (winsock2.h)
description: The ioctlsocket function (winsock2.h) controls the I/O mode of a socket and can be used on any socket in any state.
helpviewer_keywords: ["_win32_ioctlsocket_2","ioctlsocket","ioctlsocket function [Winsock]","winsock.ioctlsocket_2","winsock/ioctlsocket"]
old-location: winsock\ioctlsocket_2.htm
tech.root: WinSock
ms.assetid: 048fcb8d-acd3-4917-a997-dd133db399f8
ms.date: 08/03/2022
ms.keywords: _win32_ioctlsocket_2, ioctlsocket, ioctlsocket function [Winsock], winsock.ioctlsocket_2, winsock/ioctlsocket
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
 - ioctlsocket
 - winsock2/ioctlsocket
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ws2_32.dll
api_name:
 - ioctlsocket
---

# ioctlsocket function


## -description

The 
<b>ioctlsocket</b> function controls the I/O mode of a socket.

## -parameters

### -param s [in]

A descriptor identifying a socket.

### -param cmd [in]

A command to perform on the socket <i>s</i>.

### -param argp [in, out]

A pointer to a parameter for <i>cmd</i>.

## -returns

Upon successful completion, the 
<b>ioctlsocket</b> returns zero. Otherwise, a value of SOCKET_ERROR is returned, and a specific error code can be retrieved by calling 
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
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAENOTSOCK</a></b></dt>
</dl>
</td>
<td width="60%">
The descriptor <i>s</i> is not a socket.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEFAULT</a></b></dt>
</dl>
</td>
<td width="60%">
The <i>argp</i> parameter is not a valid part of the user address space.

</td>
</tr>
</table>

## -remarks

The 
<b>ioctlsocket</b> function can be used on any socket in any state. It is used to set or retrieve some operating parameters associated with the socket, independent of the protocol and communications subsystem. Here are the supported commands to use in the <i>cmd</i> parameter and their semantics:



The <a href="/windows/desktop/api/winsock2/nf-winsock2-wsaioctl">WSAIoctl</a> 
	 function is used to set or retrieve operating parameters associated with the socket, the transport protocol, or the communications subsystem.

The <b>WSAIoctl</b> 
	 function is more powerful than the <b>ioctlsocket</b> function and supports a large number of possible values for the operating parameters to set or retrieve.  

<h3><a id="Example_Code"></a><a id="example_code"></a><a id="EXAMPLE_CODE"></a>Example Code</h3>
The following example demonstrates the use of the <b>ioctlsocket</b> function.


```cpp

#include <winsock2.h>
#include <stdio.h>

#pragma comment(lib, "Ws2_32.lib")

void main()
{
//-------------------------
// Initialize Winsock
WSADATA wsaData;
int iResult;
u_long iMode = 0;

iResult = WSAStartup(MAKEWORD(2,2), &wsaData);
if (iResult != NO_ERROR)
  printf("Error at WSAStartup()\n");

//-------------------------
// Create a SOCKET object.
SOCKET m_socket;
m_socket = socket(AF_INET, SOCK_STREAM, IPPROTO_TCP);
if (m_socket == INVALID_SOCKET) {
  printf("Error at socket(): %ld\n", WSAGetLastError());
  WSACleanup();
  return;
}

//-------------------------
// Set the socket I/O mode: In this case FIONBIO
// enables or disables the blocking mode for the 
// socket based on the numerical value of iMode.
// If iMode = 0, blocking is enabled; 
// If iMode != 0, non-blocking mode is enabled.

iResult = ioctlsocket(m_socket, FIONBIO, &iMode);
if (iResult != NO_ERROR)
  printf("ioctlsocket failed with error: %ld\n", iResult);
  

}

```


<h3><a id="Compatibility"></a><a id="compatibility"></a><a id="COMPATIBILITY"></a>Compatibility</h3>
This 
<b>ioctlsocket</b> function performs only a subset of functions on a socket when compared to the <b>ioctl</b> function found in Berkeley sockets. The 
<b>ioctlsocket</b> function has no command parameter equivalent to the FIOASYNC of <b>ioctl</b>, and SIOCATMARK is the only socket-level command that is supported by 
<b>ioctlsocket</b>.

<b>Windows Phone 8:</b> This function is supported for Windows Phone Store apps on Windows Phone 8 and later.

<b>Windows 8.1</b> and <b>Windows Server 2012 R2</b>: This function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and later.

## -see-also

<a href="/windows/desktop/api/winsock/nf-winsock-wsaasyncselect">WSAAsyncSelect</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaeventselect">WSAEventSelect</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaioctl">WSAIoctl</a>



<a href="/windows/desktop/WinSock/winsock-functions">Winsock Functions</a>



<a href="/windows/desktop/WinSock/winsock-reference">Winsock Reference</a>



<a href="/windows/desktop/api/winsock/nf-winsock-getsockopt">getsockopt</a>



<a href="/windows/desktop/api/winsock/nf-winsock-setsockopt">setsockopt</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-socket">socket</a>
