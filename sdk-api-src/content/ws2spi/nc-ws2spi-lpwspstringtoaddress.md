---
UID: NC:ws2spi.LPWSPSTRINGTOADDRESS
title: LPWSPSTRINGTOADDRESS (ws2spi.h)
author: windows-sdk-content
description: The WSPStringToAddress function converts a human-readable numeric string to a socket address structure (sockaddr) suitable to passing to Windows Sockets routines that take such a structure.
old-location: winsock\wspstringtoaddress_2.htm
tech.root: WinSock
ms.assetid: 65cf8f7e-7ef0-472c-82d8-e8f7df9976a9
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: LPWSPSTRINGTOADDRESS, WSPStringToAddress, WSPStringToAddress function [Winsock], _win32_wspstringtoaddress_2, winsock.wspstringtoaddress_2, ws2spi/WSPStringToAddress
ms.topic: callback
f1_keywords: 
 - "ws2spi/WSPStringToAddress"
req.header: ws2spi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Ws2spi.h
api_name:
 - WSPStringToAddress
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# LPWSPSTRINGTOADDRESS callback function


## -description


The 
<b>WSPStringToAddress</b> function converts a human-readable numeric string to a socket address structure (<a href="https://docs.microsoft.com/windows/desktop/WinSock/sockaddr-2">sockaddr</a>) suitable to passing to Windows Sockets routines that take such a structure. Any missing components of the address are defaulted to a reasonable value, if possible. For example, a missing port number  defaults to zero.


## -parameters




### -param AddressString [in]

Pointer to the zero-terminated, human-readable string to convert.


### -param AddressFamily [in]

Address family to which the string belongs, or AF_UNSPEC if it is unknown.


### -param lpProtocolInfo [in]

(required) Provider's 
<a href="https://docs.microsoft.com/windows/desktop/api/winsock2/ns-winsock2-_wsaprotocol_infoa">WSAPROTOCOL_INFO</a> structure.


### -param lpAddress [out]

Buffer that is filled with a single 
<a href="https://docs.microsoft.com/windows/desktop/WinSock/sockaddr-2">sockaddr</a> structure.


### -param lpAddressLength [in, out]

Length of the Address buffer, in bytes. Returns the size of the resultant <a href="https://docs.microsoft.com/windows/desktop/WinSock/sockaddr-2">sockaddr</a> structure. If the supplied buffer is not large enough, the function fails with a specific error of <a href="https://docs.microsoft.com/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEFAULT</a> and this parameter is updated with the required size in bytes.


### -param lpErrno [out]

Pointer to the error code.


## -returns



If no error occurs, 
<b>WSPStringToAddress</b> returns zero. Otherwise, a value of SOCKET_ERROR is returned, and a specific error code is available in <i>lpErrno</i>.

<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://docs.microsoft.com/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEFAULT</a></b></dt>
</dl>
</td>
<td width="60%">
The specified address buffer is too small, pass in a larger buffer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://docs.microsoft.com/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEINVAL</a></b></dt>
</dl>
</td>
<td width="60%">
Unable to translate the string into a 
<a href="https://docs.microsoft.com/windows/desktop/WinSock/sockaddr-2">sockaddr</a>, or the provider was unable to support the indicated address family, or the specified <i>lpProtocolInfo</i> did not refer to a 
<a href="https://docs.microsoft.com/windows/desktop/api/winsock2/ns-winsock2-_wsaprotocol_infoa">WSAPROTOCOL_INFO</a> structure supported by the provider.

</td>
</tr>
</table>
 


<div> </div>





## -remarks



A layered service provider supplies an implementation of this function, but it is also a client of this function if and when it calls 
<b>WSPStringToAddress</b> of the next layer in the protocol chain. Some special considerations apply to this function's <i>lpProtocolInfo</i> parameter as it is propagated down through the layers of the protocol chain.

If the next layer in the protocol chain is another layer, then when the next layer's 
<b>WSPStringToAddress</b> is called, this layer must pass to the next layer a <i>lpProtocolInfo</i> that references the same unmodified 
<a href="https://docs.microsoft.com/windows/desktop/api/winsock2/ns-winsock2-_wsaprotocol_infoa">WSAPROTOCOL_INFO</a> structure with the same unmodified chain information. However, if the next layer is the base protocol (that is, the last element in the chain), this layer performs a substitution when calling the base provider's 
<b>WSPStringToAddress</b>. In this case, the base provider's 
<b>WSAPROTOCOL_INFO</b> structure should be referenced by the <i>lpProtocolInfo</i> parameter.

One vital benefit of this policy is that base service providers do not have to be aware of protocol chains.

This same propagation policy applies when propagating a 
<a href="https://docs.microsoft.com/windows/desktop/api/winsock2/ns-winsock2-_wsaprotocol_infoa">WSAPROTOCOL_INFO</a> structure through a layered sequence of other functions such as 
<a href="https://docs.microsoft.com/windows/desktop/api/ws2spi/nc-ws2spi-lpwspaddresstostring">WSPAddressToString</a>, 
<a href="https://docs.microsoft.com/previous-versions/windows/hardware/network/ff566282(v=vs.85)">WSPDuplicateSocket</a>, 
<a href="https://docs.microsoft.com/windows/desktop/api/ws2spi/nf-ws2spi-wspstartup">WSPStartup</a>, or 
<a href="https://docs.microsoft.com/windows/desktop/api/ws2spi/nc-ws2spi-lpwspsocket">WSPSocket</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winsock2/ns-winsock2-_wsaprotocol_infoa">WSAPROTOCOL_INFO</a>



<a href="https://docs.microsoft.com/previous-versions/windows/hardware/network/ff566282(v=vs.85)">WSPDuplicateSocket</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ws2spi/nc-ws2spi-lpwspsocket">WSPSocket</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ws2spi/nf-ws2spi-wspstartup">WSPStartup</a>



<a href="https://docs.microsoft.com/windows/desktop/WinSock/sockaddr-2">sockaddr</a>
 

 

