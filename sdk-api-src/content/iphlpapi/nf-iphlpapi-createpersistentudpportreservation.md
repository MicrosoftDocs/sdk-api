---
UID: NF:iphlpapi.CreatePersistentUdpPortReservation
title: CreatePersistentUdpPortReservation function
author: windows-sdk-content
description: Creates a persistent UDP port reservation for a consecutive block of UDP ports on the local computer.
old-location: iphlp\createpersistentudpportreservation.htm
tech.root: iphlp
ms.assetid: AFD2EFD1-55AF-49C9-8109-D4D1B7BB7C94
ms.author: windowssdkdev
ms.date: 08/15/2018
ms.keywords: CreatePersistentUdpPortReservation, CreatePersistentUdpPortReservation function [IP Helper], iphlp.createpersistentudpportreservation, iphlpapi/CreatePersistentUdpPortReservation
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Iphlpapi.dll
api_name:
 - CreatePersistentUdpPortReservation
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
<a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a> to obtain the message string for the returned error.

</td>
</tr>
</table>
 




## -remarks



The <b>CreatePersistentUdpPortReservation</b> function is defined on Windows Vista and later. 

The <b>CreatePersistentUdpPortReservation</b> function is used to add a persistent reservation for a block of UDP ports. 

Applications and services which need to reserve ports fall into two categories. The first category includes components which need a particular port as part of their operation. Such components will generally prefer to specify their required port at installation time (in an application manifest, for example). The second category includes components which need any available port or block of ports at runtime. 

These two categories correspond to specific and wildcard port reservation requests. Specific reservation requests may be persistent or runtime, while wildcard port reservation requests are only supported at runtime. 

The <b>CreatePersistentUdpPortReservation</b> function provides the ability for an application or service to reserve persistently a block of UDP ports.  Persistent TCP reservations are recorded in a persistent store for the UDP module in Windows. 

A caller obtains a persistent port reservation by specifying how many ports are required and whether a specific range is needed. If the request can be satisfied, the <b>CreatePersistentUdpPortReservation</b> function returns a unique opaque ULONG64 token, which subsequently identifies the reservation. A persistent UDP port reservation may be released by calling the <a href="https://msdn.microsoft.com/E6539B3F-48DA-41AA-8AD4-2EBBAF98069F">DeletePersistentUdpPortReservation</a> function. Note that the token for a given persistent UDP port reservation may change each time the system is restarted.



Windows does not implement inter-component security for persistent reservations obtained using these functions. This means that if a component is granted the ability to obtain any persistent port reservations, that component automatically gains the ability to consume any persistent port reservations granted to any other component on the system. Process-level security is enforced for runtime reservations, but such control cannot be extended to persistent reservations created using the created using the <a href="https://msdn.microsoft.com/19DAF828-B0E4-49E2-843D-7350C8083C45">CreatePersistentTcpPortReservation</a> or  <b>CreatePersistentUdpPortReservation</b> function.



Once a persistent UDP port reservation has been obtained, an application can request port assignments from the UDP port reservation by opening a UDP socket, then calling the <a href="https://msdn.microsoft.com/038aeca6-d7b7-4f74-ac69-4536c2e5118b">WSAIoctl</a> function specifying the <a href="https://msdn.microsoft.com/4CBFB5F8-1FA1-44BA-9932-6F0329A465CB">SIO_ASSOCIATE_PORT_RESERVATION</a> IOCTL and passing the reservation token before issuing a call to the <a href="https://msdn.microsoft.com/3a651daa-7404-4ef7-8cff-0d3dff41a8e8">bind</a> function on the socket. 

The <a href="https://msdn.microsoft.com/1A2E3920-88D2-4109-B7EF-E66BD4AB6153">SIO_ACQUIRE_PORT_RESERVATION</a> IOCTL can be used to request a runtime reservation for a block of TCP or UDP ports. For runtime port reservations, the port pool requires that reservations be consumed from the process on whose socket the reservation was granted. Runtime port reservations last only as long as the lifetime of the socket on which the <b>SIO_ACQUIRE_PORT_RESERVATION</b> IOCTL was called.  In contrast, persistent port reservations created using the <b>CreatePersistentUdpPortReservation</b> function may be consumed by any process with the ability to obtain persistent reservations. 



The <b>CreatePersistentUdpPortReservation</b> function can only be called by a user logged on as a member of the Administrators group. If <b>CreatePersistentUdpPortReservation</b> is called by a user that is not a member of the Administrators group, the function call will fail and <b>ERROR_ACCESS_DENIED</b> is returned. This function can also fail because of user account control (UAC) on Windows Vista and later. If an application that contains this function is executed by a user logged on as a member of the Administrators group other than the built-in Administrator, this call will fail unless the application has been marked in the manifest file with a <b>requestedExecutionLevel</b> set to requireAdministrator. If the application lacks this manifest file, a user logged on as a member of the Administrators group other than the built-in Administrator must then be executing the application in an enhanced shell as the built-in Administrator (RunAs administrator) for this function to succeed.






## -see-also




<a href="https://msdn.microsoft.com/19DAF828-B0E4-49E2-843D-7350C8083C45">CreatePersistentTcpPortReservation</a>



<a href="https://msdn.microsoft.com/533F8B35-6EC1-43BB-B8E6-EB086A9C646C">DeletePersistentTcpPortReservation</a>



<a href="https://msdn.microsoft.com/E6539B3F-48DA-41AA-8AD4-2EBBAF98069F">DeletePersistentUdpPortReservation</a>



<a href="https://msdn.microsoft.com/5EBEB774-13A2-49C2-92ED-5271081615AA">LookupPersistentTcpPortReservation</a>



<a href="https://msdn.microsoft.com/621C732E-9A42-455C-A1A8-F1997D6EF0D7">LookupPersistentUdpPortReservation</a>



<a href="https://msdn.microsoft.com/1A2E3920-88D2-4109-B7EF-E66BD4AB6153">SIO_ACQUIRE_PORT_RESERVATION</a>



<a href="https://msdn.microsoft.com/4CBFB5F8-1FA1-44BA-9932-6F0329A465CB">SIO_ASSOCIATE_PORT_RESERVATION</a>



<a href="https://msdn.microsoft.com/24D67A40-8CE9-4AF1-90BF-599D19C87B89">SIO_RELEASE_PORT_RESERVATION</a>



<a href="https://msdn.microsoft.com/038aeca6-d7b7-4f74-ac69-4536c2e5118b">WSAIoctl</a>



<a href="https://msdn.microsoft.com/3a651daa-7404-4ef7-8cff-0d3dff41a8e8">bind</a>
 

 

