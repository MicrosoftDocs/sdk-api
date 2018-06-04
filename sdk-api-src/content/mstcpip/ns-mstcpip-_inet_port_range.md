---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# _INET_PORT_RANGE structure


## -description


The <b>INET_PORT_RANGE</b> structure provides input data used by the <a href="https://msdn.microsoft.com/1A2E3920-88D2-4109-B7EF-E66BD4AB6153">SIO_ACQUIRE_PORT_RESERVATION</a> IOCTL to acquire a runtime reservation for a block of TCP or UDP ports.


## -struct-fields




### -field StartPort

The starting TCP or UDP port number. If this parameter is set to zero, the system will choose a starting TCP or UDP port number.


### -field NumberOfPorts

The number of TCP or UDP port numbers to reserve.


## -remarks



The  <b>INET_PORT_RANGE</b> structure is supported on Windows Vista
  and later.

The 
<b>INET_PORT_RANGE</b> structure is the datatype passed in the input buffer to the <a href="https://msdn.microsoft.com/1A2E3920-88D2-4109-B7EF-E66BD4AB6153">SIO_ACQUIRE_PORT_RESERVATION</a> IOCTL. This IOCTL is used to acquire a runtime reservation for a block of TCP or UDP ports.  

The 
<b>INET_PORT_RANGE</b> structure is typedefed to the <b>INET_PORT_RESERVATION</b> structure. 




## -see-also




<a href="https://msdn.microsoft.com/19DAF828-B0E4-49E2-843D-7350C8083C45">CreatePersistentTcpPortReservation</a>



<a href="https://msdn.microsoft.com/AFD2EFD1-55AF-49C9-8109-D4D1B7BB7C94">CreatePersistentUdpPortReservation</a>



<a href="https://msdn.microsoft.com/533F8B35-6EC1-43BB-B8E6-EB086A9C646C">DeletePersistentTcpPortReservation</a>



<a href="https://msdn.microsoft.com/E6539B3F-48DA-41AA-8AD4-2EBBAF98069F">DeletePersistentUdpPortReservation</a>



<a href="https://msdn.microsoft.com/F2332474-453F-40A3-8A0B-03A97300B724">INET_PORT_RESERVATION_INSTANCE</a>



<a href="https://msdn.microsoft.com/1AA2FF8C-BEAB-4D38-B53A-68E0628748FF">INET_PORT_RESERVATION_TOKEN</a>



<a href="https://msdn.microsoft.com/5EBEB774-13A2-49C2-92ED-5271081615AA">LookupPersistentTcpPortReservation</a>



<a href="https://msdn.microsoft.com/621C732E-9A42-455C-A1A8-F1997D6EF0D7">LookupPersistentUdpPortReservation</a>



<a href="https://msdn.microsoft.com/1A2E3920-88D2-4109-B7EF-E66BD4AB6153">SIO_ACQUIRE_PORT_RESERVATION</a>



<a href="https://msdn.microsoft.com/4CBFB5F8-1FA1-44BA-9932-6F0329A465CB">SIO_ASSOCIATE_PORT_RESERVATION</a>



<a href="https://msdn.microsoft.com/24D67A40-8CE9-4AF1-90BF-599D19C87B89">SIO_RELEASE_PORT_RESERVATION</a>
 

 

