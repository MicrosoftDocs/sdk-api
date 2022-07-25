---
UID: NC:ws2spi.LPWSPADDRESSTOSTRING
title: LPWSPADDRESSTOSTRING (ws2spi.h)
description: The LPWSPAddressToString function converts all components of a sockaddr structure into a human-readable numeric string representation of the address. This is used mainly for display purposes.
helpviewer_keywords: ["LPWSPADDRESSTOSTRING","WSPAddressToString","LPWSPAddressToString function [Winsock]","_win32_wspaddresstostring_2","winsock.wspaddresstostring_2","ws2spi/LPWSPAddressToString"]
old-location: winsock\wspaddresstostring_2.htm
tech.root: WinSock
ms.assetid: 7a6d8f77-7235-4cd1-90e1-9b5260137246
ms.date: 12/05/2018
ms.keywords: LPWSPADDRESSTOSTRING, WSPAddressToString, LPWSPAddressToString function [Winsock], _win32_wspaddresstostring_2, winsock.wspaddresstostring_2, ws2spi/LPWSPAddressToString
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - LPWSPADDRESSTOSTRING
 - ws2spi/LPWSPADDRESSTOSTRING
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Ws2spi.h
api_name:
 - LPWSPAddressToString
---

# LPWSPADDRESSTOSTRING callback function


## -description

The 
**LPWSPAddressToString** function converts all components of a 
<a href="/windows/desktop/WinSock/sockaddr-2">sockaddr</a> structure into a human-readable numeric string representation of the address. This is used mainly for display purposes.

## -parameters

### -param lpsaAddress [in]

Pointer to a 
<a href="/windows/desktop/WinSock/sockaddr-2">sockaddr</a> structure to translate into a string.

### -param dwAddressLength [in]

Length of the address of <a href="/windows/desktop/WinSock/sockaddr-2">sockaddr</a>, in bytes.

### -param lpProtocolInfo [in]

(required) 
<a href="/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa">WSAProtocol_Info</a> structure associated with the provider that will do the translation.

### -param lpszAddressString [out]

Buffer that receives the human-readable address string..

### -param lpdwAddressStringLength [in, out]

Length of the <i>AddressString</i> buffer, in bytes. Returns the length of the string actually copied into the buffer. If the supplied buffer is not large enough, the function fails with a specific error of 
<a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEFAULT</a> and this parameter is updated with the required size, in bytes.

### -param lpErrno [out]

Pointer to the error code.

## -returns

If no error occurs, 
**LPWSPAddressToString** returns zero. Otherwise, it returns SOCKET_ERROR, and a specific error code is available in <i>lpErrno</i>.

<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEFAULT</a></b></dl>
</dl>
</td>
<td width="60%">
The specified AddressString buffer is too small. Pass in a larger buffer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEINVAL</a></b></dl>
</dl>
</td>
<td width="60%">
The specified address is not a valid socket address, or its address family is not supported by the provider, or the specified <i>lpProtocolInfo</i> did not refer to a 
<a href="/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa">WSAProtocol_Info</a> structure supported by the provider.

</td>
</tr>
</table>
 


<div> </div>

## -remarks

A layered service provider supplies an implementation of this function, but it is also a client of this function if and when it calls 
**LPWSPAddressToString** of the next layer in the protocol chain. Some special considerations apply to the <i>lpProtocolInfo</i> parameter as it is propagated down through the layers of the protocol chain.

If the next layer in the protocol chain is another layer, then, when the next layer's 
**LPWSPAddressToString** is called, this layer must pass to the next layer a <i>lpProtocolInfo</i> parameter that references the same unmodified 
<a href="/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa">WSAProtocol_Info</a> structure with the same unmodified chain information. However, if the next layer is the base protocol (that is, the last element in the chain), this layer performs a substitution when calling the base provider's 
**LPWSPAddressToString**. In this case, the base provider's 
**WSAPROTOCOL_INFO** structure should be referenced by the <i>lpProtocolInfo</i> parameter. One vital benefit of this policy is that base service providers do not have to be aware of protocol chains.

This same propagation policy applies when propagating a 
<a href="/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa">WSAProtocol_Info</a> structure through a layered sequence of other functions such as 
[LPWSPDuplicateSocket](nc-ws2spi-lpwspduplicatesocket.md), 
<a href="/windows/win32/api/ws2spi/nf-ws2spi-wspstartup">WSPStartup</a>, 
[LPWSPSocket](nc-ws2spi-lpwspsocket.md), or 
[LPWSPStringToAddress](nc-ws2spi-lpwspstringtoaddress.md).

## -see-also

<a href="/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa">WSAProtocol_Info</a>



<a href="/previous-versions/windows/hardware/network/ff566282(v=vs.85)">WSPDucplicateSocket</a>



[LPWSPSocket](nc-ws2spi-lpwspsocket.md)



<a href="/windows/win32/api/ws2spi/nf-ws2spi-wspstartup">WSPStartup</a>



<a href="/windows/desktop/WinSock/sockaddr-2">sockaddr</a>