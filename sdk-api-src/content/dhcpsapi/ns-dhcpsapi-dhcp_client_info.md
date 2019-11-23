---
UID: NS:dhcpsapi._DHCP_CLIENT_INFO
title: DHCP_CLIENT_INFO (dhcpsapi.h)

description: The DHCP_CLIENT_INFO structure defines a client information record used by the DHCP server.
old-location: dhcp\dhcp_client_info.htm
tech.root: DHCP
ms.assetid: cc841dac-85d4-4250-a868-95c41731fe45

ms.date: 12/05/2018
ms.keywords: '*LPDHCP_CLIENT_INFO, DHCP_CLIENT_INFO, DHCP_CLIENT_INFO structure [DHCP], LPDHCP_CLIENT_INFO, LPDHCP_CLIENT_INFO structure pointer [DHCP], dhcp.dhcp_client_info, dhcpsapi/LPDHCP_CLIENT_INFO, dhcpsapi/_DHCP_CLIENT_INFO'
ms.topic: struct
f1_keywords:
- dhcpsapi/DHCP_CLIENT_INFO
dev_langs:
 - c++
req.header: dhcpsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
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
- HeaderDef
api_location:
- Dhcpsapi.h
api_name:
- DHCP_CLIENT_INFO
targetos: Windows
req.typenames: DHCP_CLIENT_INFO, *LPDHCP_CLIENT_INFO
req.redist: 
ms.custom: 19H1
---

# DHCP_CLIENT_INFO structure


## -description


The <b>DHCP_CLIENT_INFO</b> structure defines a client information record used by the DHCP server.


## -struct-fields




### -field ClientIpAddress


<a href="https://docs.microsoft.com/previous-versions/windows/desktop/dhcp/dhcp-server-management-type-definitions">DHCP_IP_ADDRESS</a> value that contains the assigned IP address of the DHCP client.


### -field SubnetMask


<a href="https://docs.microsoft.com/previous-versions/windows/desktop/dhcp/dhcp-server-management-type-definitions">DHCP_IP_MASK</a> value that contains the subnet mask value assigned to the DHCP client.


### -field ClientHardwareAddress


<a href="https://docs.microsoft.com/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_binary_data">DHCP_CLIENT_UID</a> structure containing the MAC address of the client's network interface device.


### -field ClientName

Unicode string that specifies the network name of the DHCP client. This member is optional.


### -field ClientComment

Unicode string that contains a comment associated with the DHCP client. This member is optional.


### -field ClientLeaseExpires


<a href="https://docs.microsoft.com/windows/desktop/api/dhcpsapi/ns-dhcpsapi-date_time">DATE_TIME</a> structure that contains the date and time the DHCP client lease will expire, in UTC time.


### -field OwnerHost


<a href="https://docs.microsoft.com/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_host_info">DHCP_HOST_INFO</a> structure that contains information on the DHCP server that assigned the IP address to the  client. 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/dhcpsapi/ns-dhcpsapi-date_time">DATE_TIME</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_client_info_array">DHCP_CLIENT_INFO_ARRAY</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_binary_data">DHCP_CLIENT_UID</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_host_info">DHCP_HOST_INFO</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpgetclientinfo">DhcpGetClientInfo</a>
 

 

