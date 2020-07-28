---
UID: NF:mswsock.GetAcceptExSockaddrs
title: GetAcceptExSockaddrs function (mswsock.h)
description: Parses the data obtained from a call to the AcceptEx function and passes the local and remote addresses to a sockaddr structure.Note  This function is a Microsoft-specific extension to the Windows Sockets specification. .
helpviewer_keywords: ["GetAcceptExSockaddrs","GetAcceptExSockaddrs function [Winsock]","_win32_getacceptexsockaddrs_2","winsock.getacceptexsockaddrs_2","winsock/GetAcceptExSockaddrs"]
old-location: winsock\getacceptexsockaddrs_2.htm
tech.root: WinSock
ms.assetid: 381ba8ab-3c99-45c8-8895-4c87949f5238
ms.date: 12/05/2018
ms.keywords: GetAcceptExSockaddrs, GetAcceptExSockaddrs function [Winsock], _win32_getacceptexsockaddrs_2, winsock.getacceptexsockaddrs_2, winsock/GetAcceptExSockaddrs
f1_keywords:
- mswsock/GetAcceptExSockaddrs
dev_langs:
- c++
req.header: mswsock.h
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
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Mswsock.dll
api_name:
- GetAcceptExSockaddrs
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GetAcceptExSockaddrs function


## -description


The 
<b>GetAcceptExSockaddrs</b> function parses the data obtained from a call to the 
<a href="https://docs.microsoft.com/windows/desktop/api/mswsock/nf-mswsock-acceptex">AcceptEx</a> function and passes the local and remote addresses to a 
<a href="https://docs.microsoft.com/windows/desktop/WinSock/sockaddr-2">sockaddr</a> structure.<div class="alert"><b>Note</b>  This function is a Microsoft-specific extension to the Windows Sockets specification.</div>
<div> </div>



## -parameters




### -param lpOutputBuffer [in]

A pointer to a buffer that receives the first block of data sent on a connection resulting from an 
<a href="https://docs.microsoft.com/windows/desktop/api/mswsock/nf-mswsock-acceptex">AcceptEx</a> call. Must be the same <i>lpOutputBuffer</i> parameter that was passed to the 
<b>AcceptEx</b>function.


### -param dwReceiveDataLength [in]

The number of bytes in the buffer used for receiving the first data. This value must be equal to the <i>dwReceiveDataLength</i> parameter that was passed to the 
<a href="https://docs.microsoft.com/windows/desktop/api/mswsock/nf-mswsock-acceptex">AcceptEx</a>function.


### -param dwLocalAddressLength [in]

The number of bytes reserved for the local address information. This value must be equal to the <i>dwLocalAddressLength</i> parameter that was passed to the 
<a href="https://docs.microsoft.com/windows/desktop/api/mswsock/nf-mswsock-acceptex">AcceptEx</a> function.


### -param dwRemoteAddressLength [in]

The number of bytes reserved for the remote address information. This value must be equal to the <i>dwRemoteAddressLength</i> parameter that was passed to the 
<a href="https://docs.microsoft.com/windows/desktop/api/mswsock/nf-mswsock-acceptex">AcceptEx</a> function.


### -param LocalSockaddr [out]

A pointer to the 
<a href="https://docs.microsoft.com/windows/desktop/WinSock/sockaddr-2">sockaddr</a> structure that receives the local address of the connection (the same information that would be returned by the 
<a href="https://docs.microsoft.com/windows/desktop/api/winsock/nf-winsock-getsockname">getsockname</a> function). This parameter must be specified.


### -param LocalSockaddrLength [out]

The size, in bytes, of the local address. This parameter must be specified.


### -param RemoteSockaddr [out]

A pointer to the <a href="https://docs.microsoft.com/windows/desktop/WinSock/sockaddr-2">sockaddr</a> structure that receives the remote address of the connection (the same information that would be returned by the 
<a href="https://docs.microsoft.com/windows/desktop/api/winsock/nf-winsock-getpeername">getpeername</a> function). This parameter must be specified.


### -param RemoteSockaddrLength [out]

The size, in bytes, of the local address. This parameter must be specified.


## -remarks



The 
<b>GetAcceptExSockaddrs</b> function is used exclusively with the 
<a href="https://docs.microsoft.com/windows/desktop/api/mswsock/nf-mswsock-acceptex">AcceptEx</a> function to parse the first data that the socket receives into local and remote addresses. The 
<b>AcceptEx</b> function returns local and remote address information in an internal format. Application developers need to use the <b>GetAcceptExSockaddrs</b> function if there is a need for the <a href="https://docs.microsoft.com/windows/desktop/WinSock/sockaddr-2">sockaddr</a> structures containing the local or remote addresses.


<div class="alert"><b>Note</b>  The function pointer for the 
<b>GetAcceptExSockaddrs</b> function must be obtained at run time by making a call to the 
<a href="https://docs.microsoft.com/windows/desktop/api/winsock2/nf-winsock2-wsaioctl">WSAIoctl</a> function with the <b>SIO_GET_EXTENSION_FUNCTION_POINTER</b> opcode specified. The input buffer passed to the <b>WSAIoctl</b> function must contain <b>WSAID_GETACCEPTEXSOCKADDRS</b>, a globally unique identifier (GUID) whose value identifies the <b>GetAcceptExSockaddrs</b> extension function. On success, the output returned by the <b>WSAIoctl</b> function contains a pointer to the <b>GetAcceptExSockaddrs</b> function. The <b>WSAID_GETACCEPTEXSOCKADDRS</b> GUID is defined in the <i>Mswsock.h</i> header file.</div>
<div> </div>


<b>Windows Phone 8:</b> This function is supported for Windows Phone Store apps on Windows Phone 8 and later.

<b>Windows 8.1</b> and <b>Windows Server 2012 R2</b>: This function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and later.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mswsock/nf-mswsock-acceptex">AcceptEx</a>



<a href="https://docs.microsoft.com/windows/desktop/WinSock/winsock-functions">Winsock Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/WinSock/winsock-reference">Winsock Reference</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winsock/nf-winsock-getpeername">getpeername</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winsock/nf-winsock-getsockname">getsockname</a>



<a href="https://docs.microsoft.com/windows/desktop/WinSock/sockaddr-2">sockaddr</a>
 

 

