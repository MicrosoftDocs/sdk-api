---
UID: NS:mstcpip.INET_PORT_RESERVATION_INSTANCE
title: INET_PORT_RESERVATION_INSTANCE
author: windows-sdk-content
description: Contains a port reservation and a token for a block of TCP or UDP ports.
old-location: winsock\inet_port_reservation_instance.htm
tech.root: WinSock
ms.assetid: F2332474-453F-40A3-8A0B-03A97300B724
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: "*PINET_PORT_RESERVATION_INSTANCE, INET_PORT_RESERVATION_INSTANCE, INET_PORT_RESERVATION_INSTANCE structure [Winsock], PINET_PORT_RESERVATION_INSTANCE, PINET_PORT_RESERVATION_INSTANCE structure pointer [Winsock], mstcpip/INET_PORT_RESERVATION_INSTANCE, mstcpip/PINET_PORT_RESERVATION_INSTANCE, winsock.inet_port_reservation_instance"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: mstcpip.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mstcpip.h
api_name:
 - INET_PORT_RESERVATION_INSTANCE
product: Windows
targetos: Windows
req.typenames: INET_PORT_RESERVATION_INSTANCE, *PINET_PORT_RESERVATION_INSTANCE
req.redist: 
---

# INET_PORT_RESERVATION_INSTANCE structure


## -description


The <b>INET_PORT_RESERVATION_INSTANCE</b> structure contains a port reservation and a token for a block of TCP or UDP ports.


## -struct-fields




### -field Reservation

A runtime port reservation for a block of TCP or UDP ports.

The <a href="https://msdn.microsoft.com/FE6946CF-61B6-422C-B9B8-5045EFAB705F">INET_PORT_RESERVATION</a> structure is typedefed to the <a href="https://msdn.microsoft.com/FE6946CF-61B6-422C-B9B8-5045EFAB705F">INET_PORT_RANGE</a> structure. 


### -field Token

A port reservation token for a block of TCP or UDP ports. 


## -remarks



The  <b>INET_PORT_RESERVATION_INSTANCE</b> structure is supported on Windows Vistaand later.

The  <b>INET_PORT_RESERVATION_INSTANCE</b> structure is returned by the <a href="https://msdn.microsoft.com/1A2E3920-88D2-4109-B7EF-E66BD4AB6153">SIO_ACQUIRE_PORT_RESERVATION</a> IOCTL when acquring a runtime reservation for a block of TCP or UDP ports.  




## -see-also




<a href="https://msdn.microsoft.com/19DAF828-B0E4-49E2-843D-7350C8083C45">CreatePersistentTcpPortReservation</a>



<a href="https://msdn.microsoft.com/AFD2EFD1-55AF-49C9-8109-D4D1B7BB7C94">CreatePersistentUdpPortReservation</a>



<a href="https://msdn.microsoft.com/533F8B35-6EC1-43BB-B8E6-EB086A9C646C">DeletePersistentTcpPortReservation</a>



<a href="https://msdn.microsoft.com/E6539B3F-48DA-41AA-8AD4-2EBBAF98069F">DeletePersistentUdpPortReservation</a>



<a href="https://msdn.microsoft.com/FE6946CF-61B6-422C-B9B8-5045EFAB705F">INET_PORT_RANGE</a>



<a href="https://msdn.microsoft.com/1AA2FF8C-BEAB-4D38-B53A-68E0628748FF">INET_PORT_RESERVATION_TOKEN</a>



<a href="https://msdn.microsoft.com/5EBEB774-13A2-49C2-92ED-5271081615AA">LookupPersistentTcpPortReservation</a>



<a href="https://msdn.microsoft.com/621C732E-9A42-455C-A1A8-F1997D6EF0D7">LookupPersistentUdpPortReservation</a>



<a href="https://msdn.microsoft.com/1A2E3920-88D2-4109-B7EF-E66BD4AB6153">SIO_ACQUIRE_PORT_RESERVATION</a>



<a href="https://msdn.microsoft.com/4CBFB5F8-1FA1-44BA-9932-6F0329A465CB">SIO_ASSOCIATE_PORT_RESERVATION</a>



<a href="https://msdn.microsoft.com/24D67A40-8CE9-4AF1-90BF-599D19C87B89">SIO_RELEASE_PORT_RESERVATION</a>
 

 

