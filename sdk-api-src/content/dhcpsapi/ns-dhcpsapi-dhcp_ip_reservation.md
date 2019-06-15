---
UID: NS:dhcpsapi._DHCP_IP_RESERVATION
title: DHCP_IP_RESERVATION (dhcpsapi.h)
author: windows-sdk-content
description: The DHCP_IP_RESERVATION structure defines a client IP reservation.
old-location: dhcp\dhcp_ip_reservation.htm
tech.root: DHCP
ms.assetid: 35d7ebc7-790b-4453-a9d4-b485f0adac46
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*LPDHCP_IP_RESERVATION, DHCP_IP_RESERVATION, DHCP_IP_RESERVATION structure [DHCP], LPDHCP_IP_RESERVATION, LPDHCP_IP_RESERVATION structure pointer [DHCP], dhcp.dhcp_ip_reservation, dhcpsapi/LPDHCP_IP_RESERVATION, dhcpsapi/_DHCP_IP_RESERVATION"
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
ms.custom: 19H1
---

# DHCP_IP_RESERVATION structure


## -description


The <b>DHCP_IP_RESERVATION</b> structure defines a client IP reservation.


## -struct-fields




### -field ReservedIpAddress


<a href="https://docs.microsoft.com/previous-versions/windows/desktop/dhcp/dhcp-server-management-type-definitions">DHCP_IP_ADDRESS</a> value that contains the reserved IP address.


### -field ReservedForClient


<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dhcpsapi/ns-dhcpsapi-_dhcp_binary_data">DHCP_CLIENT_UID</a> structure that contains information on the client holding this IP reservation.


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dhcpsapi/ns-dhcpsapi-_dhcp_binary_data">DHCP_CLIENT_UID</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/dhcp/dhcp-server-management-type-definitions">DHCP_IP_ADDRESS</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dhcpsapi/ns-dhcpsapi-_dhcp_ip_reservation_v4">DHCP_IP_RESERVATION_V4</a>
 

 

