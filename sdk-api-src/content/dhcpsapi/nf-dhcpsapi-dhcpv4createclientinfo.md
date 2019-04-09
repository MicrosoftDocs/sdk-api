---
UID: NF:dhcpsapi.DhcpV4CreateClientInfo
title: DhcpV4CreateClientInfo function (dhcpsapi.h)
author: windows-sdk-content
description: Creates a DHCPv4 client lease record in the DHCP server database.
old-location: dhcp\dhcpv4createclientinfo.htm
tech.root: DHCP
ms.assetid: 467aa6c3-9ccb-4984-8ad7-409d593ac856
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DhcpV4CreateClientInfo, DhcpV4CreateClientInfo function [DHCP], dhcp.dhcpv4createclientinfo, dhcpsapi/DhcpV4CreateClientInfo
ms.topic: function
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
 - DhcpV4CreateClientInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DhcpV4CreateClientInfo function


## -description


The <b>DhcpV4CreateClientInfo</b> function creates a DHCPv4 client lease record in the DHCP server database.


## -parameters




### -param ServerIpAddress [in, optional]

Pointer to a null-terminated Unicode string that represents the IP address or hostname of the DHCP server.


### -param ClientInfo [in]

Pointer to a <a href="https://msdn.microsoft.com/c676878d-2186-4aa2-b912-dc89272902c6">DHCP_CLIENT_INFO_PB</a> structure that contains the DHCP client lease record information. The <b>ClientIpAddress</b> and <b>ClientHardwareAddress</b> fields of this structure are required, all others are optional.


## -returns



If the function succeeds, it returns <b>ERROR_SUCCESS</b>.

If the function fails, it returns one of the following or an error code from <a href="https://msdn.microsoft.com/6370313f-d7db-4ff1-b0e0-7fa47474facb">DHCP Server Management API Error Codes</a>.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One or more of the parameters were invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
This call was performed by a client who is not a member of the <i>DHCP Administrators</i> security group.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DHCP_SUBNET_NOT_PRESENT</b></dt>
</dl>
</td>
<td width="60%">
The <b>ClientIpAddress</b> passed within <i>ClientInfo</i> does not match any DHCPv4 scope configured on the DHCP server.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DHCP_CLIENT_EXISTS</b></dt>
</dl>
</td>
<td width="60%">
The provided DHCP client record already exists in the DHCP server database.

</td>
</tr>
</table>
 




## -remarks



This function does not allow creation of leases if there is no scope corresponding to the <i>ClientIpAddress</i> configured on the server and instead returns <b>ERROR_DHCP_SUBNET_NOT_PRESENT</b>. It marks the specified client IP address as unavailable (or distributed) to avoid IP collisions. The addresses thus marked are also reflected in the scope’s address statistics.

Unlike <a href="https://msdn.microsoft.com/8b47bd52-e153-4000-9f4e-5335f029464b">DhcpCreateClientInfoVQ</a>, this function uses the <b>bClientType</b>, <b>AddressState</b>, <b>Status</b>, <b>ProbationEnds</b> and <b>QuarantineCapable</b> fields passed within the <a href="https://msdn.microsoft.com/c676878d-2186-4aa2-b912-dc89272902c6">DHCP_CLIENT_INFO_PB</a> structure to <i>ClientInfo</i> when creating the lease record. It also adds the new field <b>PolicyName</b> if passed within <i>ClientInfo</i> in the new lease record. There is no validation of whether the <b>PolicyName</b> corresponds to a valid policy configured on the DHCP server or corresponding scope.




## -see-also




<a href="https://msdn.microsoft.com/bf6df3ba-bbea-4140-960c-fb34cfe160eb">DhcpV4GetClientInfo</a>



<a href="https://msdn.microsoft.com/5d49ab90-3c40-4577-8e7e-36d1370d8de9">DhcpV6CreateClientInfo</a>
 

 

