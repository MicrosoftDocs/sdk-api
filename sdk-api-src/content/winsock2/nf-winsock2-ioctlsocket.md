---
UID: NF:winsock2.ioctlsocket
title: ioctlsocket function
author: windows-sdk-content
description: The ioctlsocket function controls the I/O mode of a socket.
old-location: winsock\ioctlsocket_2.htm
old-project: winsock
ms.assetid: 048fcb8d-acd3-4917-a997-dd133db399f8
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "_win32_ioctlsocket_2, ioctlsocket, ioctlsocket function [Winsock], winsock.ioctlsocket_2, winsock/ioctlsocket"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: WSAECOMPARATOR, *PWSAECOMPARATOR, *LPWSAECOMPARATOR
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ws2_32.dll
api_name:
 - ioctlsocket
product: Windows
targetos: Windows
req.lib: Ws2_32.lib
req.dll: Ws2_32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
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
<a href="https://msdn.microsoft.com/39e41b66-44ed-46dc-bfc2-65228b669992">WSAGetLastError</a>.

<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSANOTINITIALISED</a></b></dt>
</dl>
</td>
<td width="60%">
A successful 
<a href="https://msdn.microsoft.com/08299592-867c-491d-9769-d16602133659">WSAStartup</a> call must occur before using this function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAENETDOWN</a></b></dt>
</dl>
</td>
<td width="60%">
The network subsystem has failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAEINPROGRESS</a></b></dt>
</dl>
</td>
<td width="60%">
A blocking Windows Sockets 1.1 call is in progress, or the service provider is still processing a callback function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAENOTSOCK</a></b></dt>
</dl>
</td>
<td width="60%">
The descriptor <i>s</i> is not a socket.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAEFAULT</a></b></dt>
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



The <a href="https://msdn.microsoft.com/038aeca6-d7b7-4f74-ac69-4536c2e5118b">WSAIoctl</a> 
	 function is used to set or retrieve operating parameters associated with the socket, the transport protocol, or the communications subsystem.

The <b>WSAIoctl</b> 
	 function is more powerful than the <b>ioctlsocket</b> function and supports a large number of possible values for the operating parameters to set or retrieve.  

<h3><a id="Example_Code"></a><a id="example_code"></a><a id="EXAMPLE_CODE"></a>Example Code</h3>
The following example demonstrates the use of the <b>ioctlsocket</b> function.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
#include &lt;winsock2.h&gt;
#include &lt;stdio.h&gt;

#pragma comment(lib, "Ws2_32.lib")

void main()
{
//-------------------------
// Initialize Winsock
WSADATA wsaData;
int iResult;
u_long iMode = 0;

iResult = WSAStartup(MAKEWORD(2,2), &amp;wsaData);
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

iResult = ioctlsocket(m_socket, FIONBIO, &amp;iMode);
if (iResult != NO_ERROR)
  printf("ioctlsocket failed with error: %ld\n", iResult);
  

}
</pre>
</td>
</tr>
</table></span></div>
<h3><a id="Compatibility"></a><a id="compatibility"></a><a id="COMPATIBILITY"></a>Compatibility</h3>
This 
<b>ioctlsocket</b> function performs only a subset of functions on a socket when compared to the <b>ioctl</b> function found in Berkeley sockets. The 
<b>ioctlsocket</b> function has no command parameter equivalent to the FIOASYNC of <b>ioctl</b>, and SIOCATMARK is the only socket-level command that is supported by 
<b>ioctlsocket</b>.

<b>Windows Phone 8:</b> This function is supported for Windows Phone Store apps on Windows Phone 8 and later.

<b>Windows 8.1</b> and <b>Windows Server 2012 R2</b>: This function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and later.




## -see-also




<a href="https://msdn.microsoft.com/a4d3f599-358c-4a94-91eb-7e1c80244250">WSAAsyncSelect</a>



<a href="https://msdn.microsoft.com/f98a71e4-47fb-47a4-b37e-e4cc801a8f98">WSAEventSelect</a>



<a href="https://msdn.microsoft.com/038aeca6-d7b7-4f74-ac69-4536c2e5118b">WSAIoctl</a>



<a href="https://msdn.microsoft.com/edafb5f9-09fe-4f8e-9651-4002b6f622f4">Winsock Functions</a>



<a href="https://msdn.microsoft.com/baae2bf9-f505-4365-b60e-e3247a0218c8">Winsock Reference</a>



<a href="https://msdn.microsoft.com/25bc511d-7a9f-41c1-8983-1af1e3f8bf2d">getsockopt</a>



<a href="https://msdn.microsoft.com/3a6960c9-0c04-4403-aee1-ce250459dc30">setsockopt</a>



<a href="https://msdn.microsoft.com/6bf6e6c4-6268-479c-86a6-52e90cf317db">socket</a>
 

 

