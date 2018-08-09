---
UID: NF:dhcpsapi.DhcpV4FailoverGetClientInfo
title: DhcpV4FailoverGetClientInfo function
author: windows-sdk-content
description: Retrieves the DHCPv4 client lease information.
old-location: dhcp\dhcpv4failovergetclientinfo.htm
old-project: dhcp
ms.assetid: 125665d1-5af6-4d8f-b7fe-cdbff6a7b415
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: DhcpV4FailoverGetClientInfo, DhcpV4FailoverGetClientInfo function [DHCP], dhcp.dhcpv4failovergetclientinfo, dhcpsapi/DhcpV4FailoverGetClientInfo
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: QuarantineStatus
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Dhcpsapi.dll
api_name:
 - DhcpV4FailoverGetClientInfo
product: Windows
targetos: Windows
req.lib: Dhcpsapi.lib
req.dll: Dhcpsapi.dll
req.irql: 
---

# DhcpV4FailoverGetClientInfo function


## -description


The <b>DhcpV4FailoverGetClientInfo</b> function retrieves the DHCPv4 client lease information.


## -parameters




### -param ServerIpAddress [in, optional]

Pointer to a null-terminated Unicode string that represents the IP address or hostname of the DHCP server.


### -param SearchInfo [in]

Pointer to a <a href="https://msdn.microsoft.com/3c6f85d7-c156-4379-bad9-0705698f12e5">DHCP_SEARCH_INFO</a> structure that defines the key used to search the DHCPv4 client lease record on the server. 
If the <b>SearchType</b> member of <i>SearchInfo</i> is <b>DhcpClientName</b> and there are multiple lease records with the same client name, the server will return client information for the client with the lowest numerical IP address.



### -param ClientInfo [out]

Pointer to a <a href="https://msdn.microsoft.com/46e4fb62-5b8e-44f8-b3a0-92535ca690f0">DHCPV4_FAILOVER_CLIENT_INFO</a> structure that contains the retrieved DHCPv4 client lease record.

<div class="alert"><b>Note</b>  <p class="note">The memory for this parameter must be free using <a href="https://msdn.microsoft.com/bf22a0a6-2ecd-4460-89c4-3f870c6275dc">DhcpRpcFreeMemory</a>.

</div>
<div> </div>

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
<dt><b>ERROR_DHCP_JET_ERROR</b></dt>
</dl>
</td>
<td width="60%">
An error occurred while accessing the DHCP server database or the client entry is not present in the database.

</td>
</tr>
</table>
 



