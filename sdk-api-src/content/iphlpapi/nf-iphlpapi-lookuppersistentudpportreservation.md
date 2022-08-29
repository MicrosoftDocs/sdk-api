---
UID: NF:iphlpapi.LookupPersistentUdpPortReservation
title: LookupPersistentUdpPortReservation function (iphlpapi.h)
description: Looks up the token for a persistent UDP port reservation for a consecutive block of TCP ports on the local computer.
helpviewer_keywords: ["LookupPersistentUdpPortReservation","LookupPersistentUdpPortReservation function [IP Helper]","iphlp.lookuppersistentudpportreservation","iphlpapi/LookupPersistentUdpPortReservation"]
old-location: iphlp\lookuppersistentudpportreservation.htm
tech.root: IpHlp
ms.assetid: 621C732E-9A42-455C-A1A8-F1997D6EF0D7
ms.date: 12/05/2018
ms.keywords: LookupPersistentUdpPortReservation, LookupPersistentUdpPortReservation function [IP Helper], iphlp.lookuppersistentudpportreservation, iphlpapi/LookupPersistentUdpPortReservation
req.header: iphlpapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Iphlpapi.lib
req.dll: Iphlpapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - LookupPersistentUdpPortReservation
 - iphlpapi/LookupPersistentUdpPortReservation
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Iphlpapi.dll
api_name:
 - LookupPersistentUdpPortReservation
---

# LookupPersistentUdpPortReservation function


## -description

The 
<b>LookupPersistentUdpPortReservation</b> function looks up the token for a persistent UDP port reservation for a consecutive block of TCP ports on the local computer.

## -parameters

### -param StartPort [in]

The starting UDP port number in network byte order.

### -param NumberOfPorts [in]

The number of UDP port numbers that were reserved.

### -param Token [out]

A pointer to a port reservation token that is returned if the function succeeds.

## -returns

If the function succeeds, the return value is NO_ERROR.

If the function fails, the return value is one of the following error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
An invalid parameter was passed to the function. This error is returned if zero is passed in the <i>StartPort</i>  or <i>NumberOfPorts</i> parameters.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The element was not found. This error is returned if persistent port block specified by the <i>StartPort</i>  and <i>NumberOfPorts</i> parameters could not be found. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Other</b></dt>
</dl>
</td>
<td width="60%">
Use 
<a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> to obtain the message string for the returned error.

</td>
</tr>
</table>

## -remarks

The <b>LookupPersistentUdpPortReservation</b>  function is defined on Windows Vista and later. 

The <b>LookupPersistentUdpPortReservation</b>  function is used to lookup the token for a persistent reservation for a block of UDP ports. 

A persistent reservation for a block of UDP ports is  created by a call to the <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistentudpportreservation">CreatePersistentUdpPortReservation</a> function. The <i>StartPort</i>  or <i>NumberOfPorts</i> parameters passed to the <b>LookupPersistentUdpPortReservation</b>  function must match the values used when the persistent reservation for a block of TCP ports was created by  the <b>CreatePersistentUdpPortReservation</b> function.

If the <b>LookupPersistentUdpPortReservation</b> function succeeds, the <i>Token</i> parameter returned will point to the token for the persistent port reservation for the block of UDP ports. Note that the token for a given persistent reservation for a block of TCP ports may change each time the system is restarted.



An application can request port assignments from the UDP port reservation by opening a UDP socket, then calling the <a href="/windows/desktop/api/winsock2/nf-winsock2-wsaioctl">WSAIoctl</a> function specifying the <a href="/windows/win32/winsock/sio-associate-port-reservation">SIO_ASSOCIATE_PORT_RESERVATION</a> IOCTL and passing the reservation token before issuing a call to the <a href="/windows/desktop/api/winsock/nf-winsock-bind">bind</a> function on the socket.

## -see-also

<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistenttcpportreservation">CreatePersistentTcpPortReservation</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistentudpportreservation">CreatePersistentUdpPortReservation</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-deletepersistenttcpportreservation">DeletePersistentTcpPortReservation</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-deletepersistentudpportreservation">DeletePersistentUdpPortReservation</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-lookuppersistenttcpportreservation">LookupPersistentTcpPortReservation</a>



<a href="/windows/win32/winsock/sio-associate-port-reservation">SIO_ASSOCIATE_PORT_RESERVATION</a>