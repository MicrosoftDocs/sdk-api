---
UID: NS:dhcpsapi._DHCP_CLIENT_INFO_VQ
title: "_DHCP_CLIENT_INFO_VQ"
author: windows-sdk-content
description: Defines information about the DHCPv4 client.
old-location: dhcp\dhcp_client_info_vq.htm
old-project: DHCP
ms.assetid: f7bd832d-b4a4-404c-8959-e9653b62d434
ms.author: windowssdkdev
ms.date: 05/17/2018
ms.keywords: "*LPDHCP_CLIENT_INFO_VQ, ADDRESS_STATE_ACTIVE, ADDRESS_STATE_DECLINED, ADDRESS_STATE_DOOM, ADDRESS_STATE_OFFERED, CLIENT_TYPE_BOOTP, CLIENT_TYPE_BOTH, CLIENT_TYPE_DHCP, CLIENT_TYPE_NONE, CLIENT_TYPE_RESERVATION_FLAG, CLIENT_TYPE_UNSPECIFIED, DHCP_CLIENT_INFO_VQ, DHCP_CLIENT_INFO_VQ structure [DHCP], PDHCP_CLIENT_INFO_VQ, PDHCP_CLIENT_INFO_VQ structure pointer [DHCP], _DHCP_CLIENT_INFO_VQ, dhcp.dhcp_client_info_vq, dhcpsapi/DHCP_CLIENT_INFO_VQ, dhcpsapi/PDHCP_CLIENT_INFO_VQ"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: dhcpsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: DHCP_CLIENT_INFO_VQ, *LPDHCP_CLIENT_INFO_VQ
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Dhcpsapi.h
api_name:
 - DHCP_CLIENT_INFO_VQ
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _DHCP_CLIENT_INFO_VQ structure


## -description


The <b>DHCP_CLIENT_INFO_VQ</b> structure defines information about the DHCPv4 client.


## -struct-fields




### -field ClientIpAddress


<a href="https://msdn.microsoft.com/8e29f488-2978-43dd-b7ba-edad2e3e4b29">DHCP_IP_ADDRESS</a>type value that contains the DHCPv4 client's IPv4 address. 


### -field SubnetMask


<a href="https://msdn.microsoft.com/8e29f488-2978-43dd-b7ba-edad2e3e4b29">DHCP IP_MASK</a> type value that contains the DHCPv4 client's IPv4 subnet mask address.


### -field ClientHardwareAddress

GUID value that contains the hardware address (MAC address) of the DHCPv4 client.


### -field ClientName

Ppointer to a null-terminated Unicode string that represents the DHCPv4 client's machine name.


### -field ClientComment

Pointer to a null-terminated Unicode string that represents the description given to the DHCPv4 client.


### -field ClientLeaseExpires


<a href="https://msdn.microsoft.com/2aca69b1-b7e5-4fda-b706-ed659d86cbd5">DATE_TIME</a> structure that contains the lease expiry time for the DHCPv4 client. This is UTC time represented in the <a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> format.


### -field OwnerHost


<a href="https://msdn.microsoft.com/3d38f69d-2808-4e52-a3da-b6142578c981">DHCP_HOST_INFO</a> structure that contains information about the host machine (DHCPv4 server machine) that has provided a lease to the DHCPv4 client.


### -field bClientType

Possible types of the DHCPv4 client. The possible values are shown in the following table.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CLIENT_TYPE_UNSPECIFIED"></a><a id="client_type_unspecified"></a><dl>
<dt><b>CLIENT_TYPE_UNSPECIFIED</b></dt>
<dt>0x00</dt>
</dl>
</td>
<td width="60%">
A DHCPv4 client other than ones defined in this table.

</td>
</tr>
<tr>
<td width="40%"><a id="CLIENT_TYPE_DHCP"></a><a id="client_type_dhcp"></a><dl>
<dt><b>CLIENT_TYPE_DHCP</b></dt>
<dt>0x01</dt>
</dl>
</td>
<td width="60%">
The DHCPv4 client supports the DHCP protocol.

</td>
</tr>
<tr>
<td width="40%"><a id="CLIENT_TYPE_BOOTP"></a><a id="client_type_bootp"></a><dl>
<dt><b>CLIENT_TYPE_BOOTP</b></dt>
<dt>0x02</dt>
</dl>
</td>
<td width="60%">
The DHCPv4 client supports the BOOTP protocol.

</td>
</tr>
<tr>
<td width="40%"><a id="CLIENT_TYPE_BOTH"></a><a id="client_type_both"></a><dl>
<dt><b>CLIENT_TYPE_BOTH</b></dt>
<dt>0x03</dt>
</dl>
</td>
<td width="60%">
The DHCPv4 client understands both the DHCPv4 and the BOOTP protocols.

</td>
</tr>
<tr>
<td width="40%"><a id="CLIENT_TYPE_RESERVATION_FLAG"></a><a id="client_type_reservation_flag"></a><dl>
<dt><b>CLIENT_TYPE_RESERVATION_FLAG</b></dt>
<dt>0x04</dt>
</dl>
</td>
<td width="60%">
There is an IPv4 reservation created for the DHCPv4 client.

</td>
</tr>
<tr>
<td width="40%"><a id="CLIENT_TYPE_NONE"></a><a id="client_type_none"></a><dl>
<dt><b>CLIENT_TYPE_NONE</b></dt>
<dt>0x64</dt>
</dl>
</td>
<td width="60%">
Backward compatibility for manual addressing.

</td>
</tr>
</table>
 


### -field AddressState

Possible states of the IPv4 address given to the DHCPv4 client. The following table represents the different values and their meanings.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ADDRESS_STATE_OFFERED"></a><a id="address_state_offered"></a><dl>
<dt><b>ADDRESS_STATE_OFFERED</b></dt>
<dt>0x00</dt>
</dl>
</td>
<td width="60%">
The DHCPv4 client has been offered this IPv4 address.

</td>
</tr>
<tr>
<td width="40%"><a id="ADDRESS_STATE_ACTIVE"></a><a id="address_state_active"></a><dl>
<dt><b>ADDRESS_STATE_ACTIVE</b></dt>
<dt>0x01</dt>
</dl>
</td>
<td width="60%">
The IPv4 address is active and has an active DHCPv4 client lease record.

</td>
</tr>
<tr>
<td width="40%"><a id="ADDRESS_STATE_DECLINED"></a><a id="address_state_declined"></a><dl>
<dt><b>ADDRESS_STATE_DECLINED</b></dt>
<dt>0x02</dt>
</dl>
</td>
<td width="60%">
The IPv4 address request was declined by the DHCPv4 client; hence, it is a bad IPv4 address.

</td>
</tr>
<tr>
<td width="40%"><a id="ADDRESS_STATE_DOOM"></a><a id="address_state_doom"></a><dl>
<dt><b>ADDRESS_STATE_DOOM</b></dt>
<dt>0x03</dt>
</dl>
</td>
<td width="60%">
The IPv4 address is in DOOMED state and is due to be deleted.

</td>
</tr>
</table>
 


### -field Status


<a href="https://msdn.microsoft.com/29C165D1-9870-4398-97F9-DA1586797FF0">QuarantineStatus</a> enumeration that specifies possible health status values for the DHCPv4 client, as validated at the NAP server.


### -field ProbationEnds

This is of type <a href="https://msdn.microsoft.com/2aca69b1-b7e5-4fda-b706-ed659d86cbd5">DATE_TIME</a>, containing the end time of the probation if the DHCPv4 client is on probation. For this time period, the DHCPv4 client has full access to the network.


### -field QuarantineCapable

If <b>TRUE</b>, the DHCPv4 client is quarantine-enabled; if <b>FALSE</b>, it is not.


## -remarks



<b>DHCP_CLIENT_INFO_VQ</b> augments the DHCP_CLIENT_INFO_V5  structure by including information relating to the NAP settings of the DHCPv4 client.




## -see-also




<a href="https://msdn.microsoft.com/8e29f488-2978-43dd-b7ba-edad2e3e4b29">DHCP Server Management Type Definitions</a>



<a href="https://msdn.microsoft.com/3d38f69d-2808-4e52-a3da-b6142578c981">DHCP_HOST_INFO</a>
 

 

