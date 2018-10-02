---
UID: NS:dhcpsapi._DHCP_IP_RESERVATION
title: "_DHCP_IP_RESERVATION"
author: windows-sdk-content
description: The DHCP_IP_RESERVATION structure defines a client IP reservation.
old-location: dhcp\dhcp_ip_reservation.htm
tech.root: DHCP
ms.assetid: 35d7ebc7-790b-4453-a9d4-b485f0adac46
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: "*LPDHCP_IP_RESERVATION, DHCP_IP_RESERVATION, DHCP_IP_RESERVATION structure [DHCP], LPDHCP_IP_RESERVATION, LPDHCP_IP_RESERVATION structure pointer [DHCP], _DHCP_IP_RESERVATION, dhcp.dhcp_ip_reservation, dhcpsapi/LPDHCP_IP_RESERVATION, dhcpsapi/_DHCP_IP_RESERVATION"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: dhcpsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: Windows Server 2003
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
 - Dhcpsapi.h
api_name:
 - DHCP_IP_RESERVATION
product: Windows
targetos: Windows
req.typenames: DHCP_IP_RESERVATION, *LPDHCP_IP_RESERVATION
req.redist: 
---

# _DHCP_IP_RESERVATION structure


## -description


The <b>DHCP_IP_RESERVATION</b> structure defines a client IP reservation.


## -struct-fields




### -field ReservedIpAddress


<a href="https://msdn.microsoft.com/8e29f488-2978-43dd-b7ba-edad2e3e4b29">DHCP_IP_ADDRESS</a> value that contains the reserved IP address.


### -field ReservedForClient


<a href="https://msdn.microsoft.com/0afdddb4-12f9-4c0b-937a-2cc311c126b4">DHCP_CLIENT_UID</a> structure that contains information on the client holding this IP reservation.


## -see-also




<a href="https://msdn.microsoft.com/0afdddb4-12f9-4c0b-937a-2cc311c126b4">DHCP_CLIENT_UID</a>



<a href="https://msdn.microsoft.com/8e29f488-2978-43dd-b7ba-edad2e3e4b29">DHCP_IP_ADDRESS</a>



<a href="https://msdn.microsoft.com/01951b18-fc54-4a34-9ccd-fd98f4e7864f">DHCP_IP_RESERVATION_V4</a>
 

 

