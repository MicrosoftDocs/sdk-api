---
UID: NF:iphlpapi.CreatePersistentUdpPortReservation
title: CreatePersistentUdpPortReservation function (iphlpapi.h)
description: Creates a persistent UDP port reservation for a consecutive block of UDP ports on the local computer.
helpviewer_keywords: ["CreatePersistentUdpPortReservation","CreatePersistentUdpPortReservation function [IP Helper]","iphlp.createpersistentudpportreservation","iphlpapi/CreatePersistentUdpPortReservation"]
old-location: iphlp\createpersistentudpportreservation.htm
tech.root: IpHlp
ms.assetid: AFD2EFD1-55AF-49C9-8109-D4D1B7BB7C94
ms.date: 12/05/2018
ms.keywords: CreatePersistentUdpPortReservation, CreatePersistentUdpPortReservation function [IP Helper], iphlp.createpersistentudpportreservation, iphlpapi/CreatePersistentUdpPortReservation
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
 - CreatePersistentUdpPortReservation
 - iphlpapi/CreatePersistentUdpPortReservation
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
 - CreatePersistentUdpPortReservation
---

# CreatePersistentUdpPortReservation function


## -description

The 
<b>CreatePersistentUdpPortReservation</b> function creates a persistent UDP port reservation for a consecutive block of UDP ports on the local computer.

## -parameters

### -param StartPort [in]

The starting UDP port number in network byte order.

### -param NumberOfPorts [in]

The number of UDP port numbers to reserve.

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
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
Access is denied. This error is returned under several conditions that include the following: the  user lacks the required administrative privileges on the local computer or the application is not running in an enhanced shell as the built-in Administrator (RunAs administrator).  

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
An invalid parameter was passed to the function. 

This error is returned if zero is passed in the <i>StartPort</i>  or <i>NumberOfPorts</i> parameters. This error is also returned if the <i>NumberOfPorts</i> parameter is too large a block of ports depending on the <i>StartPort</i> parameter that the allocable block of ports would exceed the maximum port that can be allocated.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SHARING_VIOLATION</b></dt>
</dl>
</td>
<td width="60%">
The process cannot access the file because it is being used by another process. This error is returned if a UDP port in the block of UDP ports specified by the <i>StartPort</i>  and <i>NumberOfPorts</i> parameters is already being used. This error is also returned if a persistent reservation for a block of UDP ports specified by the <i>StartPort</i>  and <i>NumberOfPorts</i> parameters matches or overlaps a persistent reservation for a block of UDP ports that was already created. 

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

The <b>CreatePersistentUdpPortReservation</b> function is defined on Windows Vista and later. 

The <b>CreatePersistentUdpPortReservation</b> function is used to add a persistent reservation for a block of UDP ports. 

Applications and services which need to reserve ports fall into two categories. The first category includes components which need a particular port as part of their operation. Such components will generally prefer to specify their required port at installation time (in an application manifest, for example). The second category includes components which need any available port or block of ports at runtime. 

These two categories correspond to specific and wildcard port reservation requests. Specific reservation requests may be persistent or runtime, while wildcard port reservation requests are only supported at runtime. 

The <b>CreatePersistentUdpPortReservation</b> function provides the ability for an application or service to reserve persistently a block of UDP ports.  Persistent TCP reservations are recorded in a persistent store for the UDP module in Windows. 

A caller obtains a persistent port reservation by specifying how many ports are required and whether a specific range is needed. If the request can be satisfied, the <b>CreatePersistentUdpPortReservation</b> function returns a unique opaque ULONG64 token, which subsequently identifies the reservation. A persistent UDP port reservation may be released by calling the <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-deletepersistentudpportreservation">DeletePersistentUdpPortReservation</a> function. Note that the token for a given persistent UDP port reservation may change each time the system is restarted.



Windows does not implement inter-component security for persistent reservations obtained using these functions. This means that if a component is granted the ability to obtain any persistent port reservations, that component automatically gains the ability to consume any persistent port reservations granted to any other component on the system. Process-level security is enforced for runtime reservations, but such control cannot be extended to persistent reservations created using the created using the <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistenttcpportreservation">CreatePersistentTcpPortReservation</a> or  <b>CreatePersistentUdpPortReservation</b> function.



Once a persistent UDP port reservation has been obtained, an application can request port assignments from the UDP port reservation by opening a UDP socket, then calling the <a href="/windows/desktop/api/winsock2/nf-winsock2-wsaioctl">WSAIoctl</a> function specifying the <a href="/windows/win32/winsock/sio-associate-port-reservation">SIO_ASSOCIATE_PORT_RESERVATION</a> IOCTL and passing the reservation token before issuing a call to the <a href="/windows/desktop/api/winsock/nf-winsock-bind">bind</a> function on the socket. 

The <a href="/windows/win32/winsock/sio-acquire-port-reservation">SIO_ACQUIRE_PORT_RESERVATION</a> IOCTL can be used to request a runtime reservation for a block of TCP or UDP ports. For runtime port reservations, the port pool requires that reservations be consumed from the process on whose socket the reservation was granted. Runtime port reservations last only as long as the lifetime of the socket on which the <b>SIO_ACQUIRE_PORT_RESERVATION</b> IOCTL was called.  In contrast, persistent port reservations created using the <b>CreatePersistentUdpPortReservation</b> function may be consumed by any process with the ability to obtain persistent reservations. 



The <b>CreatePersistentUdpPortReservation</b> function can only be called by a user logged on as a member of the Administrators group. If <b>CreatePersistentUdpPortReservation</b> is called by a user that is not a member of the Administrators group, the function call will fail and <b>ERROR_ACCESS_DENIED</b> is returned. This function can also fail because of user account control (UAC) on Windows Vista and later. If an application that contains this function is executed by a user logged on as a member of the Administrators group other than the built-in Administrator, this call will fail unless the application has been marked in the manifest file with a <b>requestedExecutionLevel</b> set to requireAdministrator. If the application lacks this manifest file, a user logged on as a member of the Administrators group other than the built-in Administrator must then be executing the application in an enhanced shell as the built-in Administrator (RunAs administrator) for this function to succeed.

## -see-also

<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistenttcpportreservation">CreatePersistentTcpPortReservation</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-deletepersistenttcpportreservation">DeletePersistentTcpPortReservation</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-deletepersistentudpportreservation">DeletePersistentUdpPortReservation</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-lookuppersistenttcpportreservation">LookupPersistentTcpPortReservation</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-lookuppersistentudpportreservation">LookupPersistentUdpPortReservation</a>



<a href="/windows/win32/winsock/sio-acquire-port-reservation">SIO_ACQUIRE_PORT_RESERVATION</a>



<a href="/windows/win32/winsock/sio-associate-port-reservation">SIO_ASSOCIATE_PORT_RESERVATION</a>



<a href="/windows/win32/winsock/sio-release-port-reservation">SIO_RELEASE_PORT_RESERVATION</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaioctl">WSAIoctl</a>



<a href="/windows/desktop/api/winsock/nf-winsock-bind">bind</a>