---
UID: NC:ws2spi.LPWSPADDRESSTOSTRING
title: LPWSPADDRESSTOSTRING (ws2spi.h)
author: windows-sdk-content
description: The WSPAddressToString function converts all components of a sockaddr structure into a human readableâ€“numeric string representation of the address. This is used mainly for display purposes.
old-location: winsock\wspaddresstostring_2.htm
tech.root: WinSock
ms.assetid: 7a6d8f77-7235-4cd1-90e1-9b5260137246
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: LPWSPADDRESSTOSTRING, WSPAddressToString, WSPAddressToString function [Winsock], _win32_wspaddresstostring_2, winsock.wspaddresstostring_2, ws2spi/WSPAddressToString
ms.topic: callback
f1_keywords:
- ws2spi/WSPAddressToString
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
- WSPAddressToString
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# LPWSPADDRESSTOSTRING callback function


## -description


The 
<b>WSPAddressToString</b> function converts all components of a 
<a href="https://docs.microsoft.com/windows/desktop/WinSock/sockaddr-2">sockaddr</a> structure into a human readableâ€“numeric string representation of the address. This is used mainly for display purposes.


## -parameters




### -param lpsaAddress [in]

Pointer to a 
<a href="https://docs.microsoft.com/windows/desktop/WinSock/sockaddr-2">sockaddr</a> structure to translate into a string.


### -param dwAddressLength [in]

Length of the address of <a href="https://docs.microsoft.com/windows/desktop/WinSock/sockaddr-2">sockaddr</a>, in bytes.


### -param lpProtocolInfo [in]

(required) 
<a href="https://docs.microsoft.com/windows/desktop/api/winsock2/ns-winsock2-wsaprotocol_infoa">WSAPROTOCOL_INFO</a> structure associated with the provider that will do the translation.


### -param lpszAddressString [out]

Buffer that receives the human readableâ€“address string..


### -param lpdwAddressStringLength [in, out]

Length of the <i>AddressString</i> buffer, in bytes. Returns the length of the string actually copied into the buffer. If the supplied buffer is not large enough, the function fails with a specific error of 
<a href="https://docs.microsoft.com/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEFAULT</a> and this parameter is updated with the required size, in bytes.


### -param lpErrno [out]

Pointer to the error code.


## -returns



If no error occurs, 
<b>WSPAddressToString</b> returns zero. Otherwise, it returns SOCKET_ERROR, and a specific error code is available in <i>lpErrno</i>.

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
The specified AddressString buffer is too small. Pass in a larger buffer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://docs.microsoft.com/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEINVAL</a></b></dt>
</dl>
</td>
<td width="60%">
The specified address is not a valid socket address, or its address family is not supported by the provider, or the specified <i>lpProtocolInfo</i> did not refer to a 
<a href="https://docs.microsoft.com/windows/desktop/api/winsock2/ns-winsock2-wsaprotocol_infoa">WSAPROTOCOL_INFO</a> structure supported by the provider.

</td>
</tr>
</table>
 


<div> </div>





## -remarks



A layered service provider supplies an implementation of this function, but it is also a client of this function if and when it calls 
<b>WSPAddressToString</b> of the next layer in the protocol chain. Some special considerations apply to the <i>lpProtocolInfo</i> parameter as it is propagated down through the layers of the protocol chain.

If the next layer in the protocol chain is another layer, then, when the next layer's 
<b>WSPAddressToString</b> is called, this layer must pass to the next layer a <i>lpProtocolInfo</i> parameter that references the same unmodified 
<a href="https://docs.microsoft.com/windows/desktop/api/winsock2/ns-winsock2-wsaprotocol_infoa">WSAPROTOCOL_INFO</a> structure with the same unmodified chain information. However, if the next layer is the base protocol (that is, the last element in the chain), this layer performs a substitution when calling the base provider's 
<b>WSPAddressToString</b>. In this case, the base provider's 
<b>WSAPROTOCOL_INFO</b> structure should be referenced by the <i>lpProtocolInfo</i> parameter. One vital benefit of this policy is that base service providers do not have to be aware of protocol chains.

This same propagation policy applies when propagating a 
<a href="https://docs.microsoft.com/windows/desktop/api/winsock2/ns-winsock2-wsaprotocol_infoa">WSAPROTOCOL_INFO</a> structure through a layered sequence of other functions such as 
<a href="https://docs.microsoft.com/previous-versions/windows/hardware/network/ff566282(v=vs.85)">WSPDuplicateSocket</a>, 
<a href="https://docs.microsoft.com/windows/desktop/api/ws2spi/nf-ws2spi-wspstartup">WSPStartup</a>, 
<a href="https://docs.microsoft.com/windows/desktop/api/ws2spi/nc-ws2spi-lpwspsocket">WSPSocket</a>, or 
<a href="https://docs.microsoft.com/windows/desktop/api/ws2spi/nc-ws2spi-lpwspstringtoaddress">WSPStringToAddress</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winsock2/ns-winsock2-wsaprotocol_infoa">WSAPROTOCOL_INFO</a>



<a href="https://docs.microsoft.com/previous-versions/windows/hardware/network/ff566282(v=vs.85)">WSPDucplicateSocket</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ws2spi/nc-ws2spi-lpwspsocket">WSPSocket</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ws2spi/nf-ws2spi-wspstartup">WSPStartup</a>



<a href="https://docs.microsoft.com/windows/desktop/WinSock/sockaddr-2">sockaddr</a>
 

 

