---
UID: NF:iphlpapi.LookupPersistentUdpPortReservation
title: LookupPersistentUdpPortReservation function
author: windows-sdk-content
description: Looks up the token for a persistent UDP port reservation for a consecutive block of TCP ports on the local computer.
old-location: iphlp\lookuppersistentudpportreservation.htm
tech.root: iphlp
ms.assetid: 621C732E-9A42-455C-A1A8-F1997D6EF0D7
ms.author: windowssdkdev
ms.date: 08/15/2018
ms.keywords: LookupPersistentUdpPortReservation, LookupPersistentUdpPortReservation function [IP Helper], iphlp.lookuppersistentudpportreservation, iphlpapi/LookupPersistentUdpPortReservation
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
 - LookupPersistentUdpPortReservation
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
<a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a> to obtain the message string for the returned error.

</td>
</tr>
</table>
 




## -remarks



The <b>LookupPersistentUdpPortReservation</b>  function is defined on Windows Vista and later. 

The <b>LookupPersistentUdpPortReservation</b>  function is used to lookup the token for a persistent reservation for a block of UDP ports. 

A persistent reservation for a block of UDP ports is  created by a call to the <a href="https://msdn.microsoft.com/AFD2EFD1-55AF-49C9-8109-D4D1B7BB7C94">CreatePersistentUdpPortReservation</a> function. The <i>StartPort</i>  or <i>NumberOfPorts</i> parameters passed to the <b>LookupPersistentUdpPortReservation</b>  function must match the values used when the persistent reservation for a block of TCP ports was created by  the <b>CreatePersistentUdpPortReservation</b> function.

If the <b>LookupPersistentUdpPortReservation</b> function succeeds, the <i>Token</i> parameter returned will point to the token for the persistent port reservation for the block of UDP ports. Note that the token for a given persistent reservation for a block of TCP ports may change each time the system is restarted.



An application can request port assignments from the UDP port reservation by opening a UDP socket, then calling the <a href="https://msdn.microsoft.com/038aeca6-d7b7-4f74-ac69-4536c2e5118b">WSAIoctl</a> function specifying the <a href="https://msdn.microsoft.com/4CBFB5F8-1FA1-44BA-9932-6F0329A465CB">SIO_ASSOCIATE_PORT_RESERVATION</a> IOCTL and passing the reservation token before issuing a call to the <a href="https://msdn.microsoft.com/3a651daa-7404-4ef7-8cff-0d3dff41a8e8">bind</a> function on the socket. 




## -see-also




<a href="https://msdn.microsoft.com/19DAF828-B0E4-49E2-843D-7350C8083C45">CreatePersistentTcpPortReservation</a>



<a href="https://msdn.microsoft.com/AFD2EFD1-55AF-49C9-8109-D4D1B7BB7C94">CreatePersistentUdpPortReservation</a>



<a href="https://msdn.microsoft.com/533F8B35-6EC1-43BB-B8E6-EB086A9C646C">DeletePersistentTcpPortReservation</a>



<a href="https://msdn.microsoft.com/E6539B3F-48DA-41AA-8AD4-2EBBAF98069F">DeletePersistentUdpPortReservation</a>



<a href="https://msdn.microsoft.com/5EBEB774-13A2-49C2-92ED-5271081615AA">LookupPersistentTcpPortReservation</a>



<a href="https://msdn.microsoft.com/4CBFB5F8-1FA1-44BA-9932-6F0329A465CB">SIO_ASSOCIATE_PORT_RESERVATION</a>
 

 

