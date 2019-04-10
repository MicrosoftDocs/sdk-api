---
UID: NF:dhcpsapi.DhcpRemoveSubnetElement
title: DhcpRemoveSubnetElement function (dhcpsapi.h)
author: windows-sdk-content
description: Removes an IPv4 subnet element from an IPv4 subnet defined on the DHCPv4 server.
old-location: dhcp\dhcpremovesubnetelement.htm
tech.root: DHCP
ms.assetid: b27de25f-c96d-4881-9788-495ffe220d61
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DhcpRemoveSubnetElement, DhcpRemoveSubnetElement function [DHCP], dhcp.dhcpremovesubnetelement, dhcpsapi/DhcpRemoveSubnetElement
ms.topic: function
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
req.lib: Dhcpsapi.lib
req.dll: Dhcpsapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Dhcpsapi.dll
api_name:
 - DhcpRemoveSubnetElement
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DhcpRemoveSubnetElement function


## -description


The <b>DhcpRemoveSubnetElement</b> function removes an IPv4 subnet element from an IPv4 subnet defined on the DHCPv4 server.


## -parameters




### -param ServerIpAddress [in]

Unicode string that specifies the IP address or hostname of the DHCPv4 server.


### -param SubnetAddress [in]


<a href="https://msdn.microsoft.com/8e29f488-2978-43dd-b7ba-edad2e3e4b29">DHCP_IP_ADDRESS</a> value that specifies the IPv4 address of the subnet gateway from which elements are to be removed.


### -param RemoveElementInfo [in]


<a href="https://msdn.microsoft.com/d6c32be0-a080-42c1-b9bf-3f5da2c4dbe0">DHCP_SUBNET_ELEMENT_DATA</a> structure that contains information used to find the element that will be removed from subnet specified in <i>SubnetAddress</i>.


### -param ForceFlag [in]


<a href="https://msdn.microsoft.com/2ec45a99-432d-4218-9048-81714ceff36b">DHCP_FORCE_FLAG</a> enumeration value that indicates whether or not the clients affected by the removal of the subnet element should also be deleted.

<div class="alert"><b>Note</b>  If the flag is set to <b>DhcpNoForce</b> and this subnet has served an IPv4 address to DHCPv4/BOOTP clients, the IPv4 range is not deleted; conversely, if the flag is set to <b>DhcpFullForce</b>, the IPv4 range is deleted along with the DHCPv4 client lease record on the DHCPv4 server.</div>
<div> </div>

## -returns



This function returns <b>ERROR_SUCCESS</b> upon a successful call. Otherwise, it returns one of the <a href="https://msdn.microsoft.com/6370313f-d7db-4ff1-b0e0-7fa47474facb">DHCP Server Management API Error Codes</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DHCP_JET_ERROR</b></dt>
</dl>
</td>
<td width="60%">
An error occurred while accessing the DHCP server database.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DHCP_SUBNET_NOT_PRESENT</b></dt>
</dl>
</td>
<td width="60%">
The specified IPv4 subnet is not defined on the DHCP server.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DHCP_RESERVED_CLIENT</b></dt>
</dl>
</td>
<td width="60%">
The specified DHCP client is a reserved client.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DHCP_INVALID_RANGE</b></dt>
</dl>
</td>
<td width="60%">
The specified IPv4 address range either overlaps an existing IPv4 address range, or is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DHCP_ELEMENT_CANT_REMOVE</b></dt>
</dl>
</td>
<td width="60%">
At least one multicast IPv4 address has been leased out to a MADCAP client.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/2ec45a99-432d-4218-9048-81714ceff36b">DHCP_FORCE_FLAG</a>



<a href="https://msdn.microsoft.com/d6c32be0-a080-42c1-b9bf-3f5da2c4dbe0">DHCP_SUBNET_ELEMENT_DATA</a>



<a href="https://msdn.microsoft.com/4f93d4e8-f41e-4df8-98cc-70a11be75eab">DhcpAddSubnetElement</a>
 

 

