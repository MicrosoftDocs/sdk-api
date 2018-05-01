---
UID: NF:dhcpsapi.DhcpV4GetClientInfo
title: DhcpV4GetClientInfo function
author: windows-driver-content
description: Retrieves DHCP client lease record information from the DHCP server database.
old-location: dhcp\dhcpv4getclientinfo.htm
old-project: DHCP
ms.assetid: bf6df3ba-bbea-4140-960c-fb34cfe160eb
ms.author: windowsdriverdev
ms.date: 4/7/2018
ms.keywords: DhcpV4GetClientInfo, DhcpV4GetClientInfo function [DHCP], dhcp.dhcpv4getclientinfo, dhcpsapi/DhcpV4GetClientInfo
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: QuarantineStatus
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Dhcpsapi.dll
api_name:
-	DhcpV4GetClientInfo
product: Windows
targetos: Windows
req.lib: Dhcpsapi.lib
req.dll: Dhcpsapi.dll
req.irql: 
---

# DhcpV4GetClientInfo function


## -description


The <b>DhcpV4GetClientInfo</b> function retrieves DHCP client lease record information from the DHCP server database.


## -parameters




### -param ServerIpAddress [in, optional]

Pointer to a null-terminated Unicode string that represents the IP address or hostname of the DHCP server.


### -param SearchInfo [in]

Pointer to a <a href="https://msdn.microsoft.com/3c6f85d7-c156-4379-bad9-0705698f12e5">DHCP_SEARCH_INFO</a> structure that defines the key used to search for the client lease record on the DHCP server.


### -param ClientInfo [out]

Pointer to a <a href="https://msdn.microsoft.com/3ee224fb-650f-4468-848b-960424202ac3">DHCP_CLIENT_INFO_PB</a> structure that returns the DHCP client lease record information.


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
Invalid or NULL <i>SearchInfo</i> was passed to the function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
This call was performed by a client that is not a member of the <i>DHCP Users</i> or  <i>DHCP Administrators</i> security groups.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DHCP_INVALID_DHCP_CLIENT</b></dt>
</dl>
</td>
<td width="60%">
The DHCP client is not valid. In this case, the search information passed had no corresponding IPv4 lease records.

</td>
</tr>
</table>
 




## -remarks



If the <b>SearchType</b> member of the structure passed to <i>SearchInfo</i> is <b>DhcpClientName</b> and there are multiple lease records with the same client hostnames, the lease record returned is indeterminate.

<i>ClientInfo</i> should be free using <a href="https://msdn.microsoft.com/bf22a0a6-2ecd-4460-89c4-3f870c6275dc">DhcpRpcFreeMemory</a>.




## -see-also




<a href="https://msdn.microsoft.com/467aa6c3-9ccb-4984-8ad7-409d593ac856">DhcpV4CreateClientInfo</a>



<a href="https://msdn.microsoft.com/bf6df3ba-bbea-4140-960c-fb34cfe160eb">DhcpV4GetClientInfo</a>



<a href="https://msdn.microsoft.com/5d49ab90-3c40-4577-8e7e-36d1370d8de9">DhcpV6CreateClientInfo</a>
 

 

