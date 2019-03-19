---
UID: NS:dhcpsapi._DHCP_IP_RESERVATION_INFO
title: DHCP_IP_RESERVATION_INFO (dhcpsapi.h)
author: windows-sdk-content
description: The DHCP_IP_RESERVATION_INFO structure defines an IPv4 reservation for a DHCPv4 client.
old-location: dhcp\dhcp_ip_reservation_info.htm
tech.root: DHCP
ms.assetid: 4f0110b5-3770-4aae-8df7-d2481eac3417
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*LPDHCP_IP_RESERVATION_INFO, CLIENT_TYPE_BOOTP, CLIENT_TYPE_BOTH, CLIENT_TYPE_DHCP, DHCP_IP_RESERVATION_INFO, DHCP_IP_RESERVATION_INFO structure [DHCP], LPDHCP_IP_RESERVATION_INFO, LPDHCP_IP_RESERVATION_INFO structure pointer [DHCP], dhcp.dhcp_ip_reservation_info, dhcpsapi/DHCP_IP_RESERVATION_INFO, dhcpsapi/LPDHCP_IP_RESERVATION_INFO"
ms.topic: struct
req.header: dhcpsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - dhcpsapi.h
api_name:
 - DHCP_IP_RESERVATION_INFO
product: Windows
targetos: Windows
req.typenames: DHCP_IP_RESERVATION_INFO, *LPDHCP_IP_RESERVATION_INFO
req.redist: 
---

# DHCP_IP_RESERVATION_INFO structure


## -description


The <b>DHCP_IP_RESERVATION_INFO</b> structure defines an IPv4 reservation for a DHCPv4 client. It extends the <a href="https://msdn.microsoft.com/01951b18-fc54-4a34-9ccd-fd98f4e7864f">DHCP_IP_RESERVATION_V4</a> structure by including the reservation client name and description.


## -struct-fields




### -field ReservedIpAddress


<a href="https://msdn.microsoft.com/8e29f488-2978-43dd-b7ba-edad2e3e4b29">DHCP_IP_ADDRESS</a> structure that contains the reserved IP address.


### -field ReservedForClient


<a href="https://msdn.microsoft.com/0afdddb4-12f9-4c0b-937a-2cc311c126b4">DHCP_CLIENT_UID</a> structure that contains the hardware address (MAC address) of the DHCPv4 client that holds this reservation.


### -field ReservedClientName

Pointer to a null-terminated Unicode string that represents the DHCPv4 reserved client machine name.


### -field ReservedClientDesc

Pointer to a null-terminated Unicode string that represents the description of the DHCPv4 reserved client.


### -field bAllowedClientTypes

Value that specifies the DHCPv4 reserved client type. The possible values are below:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CLIENT_TYPE_DHCP"></a><a id="client_type_dhcp"></a><dl>
<dt><b>CLIENT_TYPE_DHCP</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The DHCPv4 client supports the DHCP protocol only.

</td>
</tr>
<tr>
<td width="40%"><a id="CLIENT_TYPE_BOOTP"></a><a id="client_type_bootp"></a><dl>
<dt><b>CLIENT_TYPE_BOOTP</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The DHCPv4 client supports the BOOTP protocol only.

</td>
</tr>
<tr>
<td width="40%"><a id="CLIENT_TYPE_BOTH"></a><a id="client_type_both"></a><dl>
<dt><b>CLIENT_TYPE_BOTH</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
The DHCPv4 client supports both the DHCPv4 and the BOOTP protocols.

</td>
</tr>
</table>
 


### -field fOptionsPresent

<b>TRUE</b> if  the DHCPv4 reserved client has options configured at reservation level. Otherwise, it is <b>FALSE</b>. 


## -see-also




<a href="https://msdn.microsoft.com/01951b18-fc54-4a34-9ccd-fd98f4e7864f">DHCP_IP_RESERVATION_V4</a>



<a href="https://msdn.microsoft.com/f1595632-018b-4626-b3c6-49f0e5b3752c">DHCP_IP_RESERVATION_V6</a>



<a href="https://msdn.microsoft.com/9823ee47-6b61-4256-8fac-d301d72774ec">DHCP_RESERVATION_INFO_ARRAY</a>
 

 

