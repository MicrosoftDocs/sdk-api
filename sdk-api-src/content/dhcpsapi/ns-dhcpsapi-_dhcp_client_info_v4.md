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

# _DHCP_CLIENT_INFO_V4 structure


## -description


The <b>DHCP_CLIENT_INFO_V4</b> structure defines a client information record used by the DHCP server, extending the definition provided in <a href="https://msdn.microsoft.com/cc841dac-85d4-4250-a868-95c41731fe45">DHCP_CLIENT_INFO</a> by including client type information. 


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


### -field bClientType

Specifies the types of dynamic IP address service used by the client.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CLIENT_TYPE_UNSPECIFIED"></a><a id="client_type_unspecified"></a><dl>
<dt><b>CLIENT_TYPE_UNSPECIFIED</b></dt>
</dl>
</td>
<td width="60%">
The client's dynamic IP address protocol is unknown.

</td>
</tr>
<tr>
<td width="40%"><a id="CLIENT_TYPE_DHCP"></a><a id="client_type_dhcp"></a><dl>
<dt><b>CLIENT_TYPE_DHCP</b></dt>
</dl>
</td>
<td width="60%">
The client uses DHCP for dynamic IP address service.

</td>
</tr>
<tr>
<td width="40%"><a id="CLIENT_TYPE_BOOTP"></a><a id="client_type_bootp"></a><dl>
<dt><b>CLIENT_TYPE_BOOTP</b></dt>
</dl>
</td>
<td width="60%">
The client uses BOOTP for dynamic IP address service.

</td>
</tr>
<tr>
<td width="40%"><a id="CLIENT_TYPE_BOTH"></a><a id="client_type_both"></a><dl>
<dt><b>CLIENT_TYPE_BOTH</b></dt>
</dl>
</td>
<td width="60%">
The client can use either DHCP or BOOTP for dynamic IP address service.

</td>
</tr>
<tr>
<td width="40%"><a id="CLIENT_TYPE_NONE"></a><a id="client_type_none"></a><dl>
<dt><b>CLIENT_TYPE_NONE</b></dt>
</dl>
</td>
<td width="60%">
The client does not use a supported dynamic IP address service.

</td>
</tr>
</table>
 


## -see-also




<a href="https://msdn.microsoft.com/2aca69b1-b7e5-4fda-b706-ed659d86cbd5">DATE_TIME</a>



<a href="https://msdn.microsoft.com/cda4bf44-0a4c-4825-ae3f-379ceae5aadb">DHCP_CLIENT_INFO_ARRAY_V4</a>



<a href="https://msdn.microsoft.com/0afdddb4-12f9-4c0b-937a-2cc311c126b4">DHCP_CLIENT_UID</a>



<a href="https://msdn.microsoft.com/3d38f69d-2808-4e52-a3da-b6142578c981">DHCP_HOST_INFO</a>



<a href="https://msdn.microsoft.com/3f8b9cbb-f903-4a97-8a38-caf2210b6d48">DhcpGetClientInfoV4</a>
 

 

