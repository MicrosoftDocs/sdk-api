---
UID: NS:dhcpsapi._DHCP_CLIENT_INFO
title: "_DHCP_CLIENT_INFO"
author: windows-sdk-content
description: The DHCP_CLIENT_INFO structure defines a client information record used by the DHCP server.
old-location: dhcp\dhcp_client_info.htm
old-project: DHCP
ms.assetid: cc841dac-85d4-4250-a868-95c41731fe45
ms.author: windowssdkdev
ms.date: 05/17/2018
ms.keywords: "*LPDHCP_CLIENT_INFO, DHCP_CLIENT_INFO, DHCP_CLIENT_INFO structure [DHCP], LPDHCP_CLIENT_INFO, LPDHCP_CLIENT_INFO structure pointer [DHCP], _DHCP_CLIENT_INFO, dhcp.dhcp_client_info, dhcpsapi/LPDHCP_CLIENT_INFO, dhcpsapi/_DHCP_CLIENT_INFO"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: DHCP_CLIENT_INFO, *LPDHCP_CLIENT_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Dhcpsapi.h
api_name:
-	DHCP_CLIENT_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _DHCP_CLIENT_INFO structure


## -description


The <b>DHCP_CLIENT_INFO</b> structure defines a client information record used by the DHCP server.


## -struct-fields




### -field ClientIpAddress


<a href="https://msdn.microsoft.com/8e29f488-2978-43dd-b7ba-edad2e3e4b29">DHCP_IP_ADDRESS</a> value that contains the assigned IP address of the DHCP client.


### -field SubnetMask


<a href="https://msdn.microsoft.com/8e29f488-2978-43dd-b7ba-edad2e3e4b29">DHCP_IP_MASK</a> value that contains the subnet mask value assigned to the DHCP client.


### -field ClientHardwareAddress


<a href="https://msdn.microsoft.com/0afdddb4-12f9-4c0b-937a-2cc311c126b4">DHCP_CLIENT_UID</a> structure containing the MAC address of the client's network interface device.


### -field ClientName

Unicode string that specifies the network name of the DHCP client. This member is optional.


### -field ClientComment

Unicode string that contains a comment associated with the DHCP client. This member is optional.


### -field ClientLeaseExpires


<a href="https://msdn.microsoft.com/2aca69b1-b7e5-4fda-b706-ed659d86cbd5">DATE_TIME</a> structure that contains the date and time the DHCP client lease will expire, in UTC time.


### -field OwnerHost


<a href="https://msdn.microsoft.com/3d38f69d-2808-4e52-a3da-b6142578c981">DHCP_HOST_INFO</a> structure that contains information on the DHCP server that assigned the IP address to the  client. 


## -see-also




<a href="https://msdn.microsoft.com/2aca69b1-b7e5-4fda-b706-ed659d86cbd5">DATE_TIME</a>



<a href="https://msdn.microsoft.com/32bb0664-5227-4c84-a2d8-c3b348ae451c">DHCP_CLIENT_INFO_ARRAY</a>



<a href="https://msdn.microsoft.com/0afdddb4-12f9-4c0b-937a-2cc311c126b4">DHCP_CLIENT_UID</a>



<a href="https://msdn.microsoft.com/3d38f69d-2808-4e52-a3da-b6142578c981">DHCP_HOST_INFO</a>



<a href="https://msdn.microsoft.com/67095868-7e02-4d82-b2f0-70c413fa8ed6">DhcpGetClientInfo</a>
 

 

