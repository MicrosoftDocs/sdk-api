---
UID: NF:dhcpsapi.DhcpGetFilterV4
title: DhcpGetFilterV4 function
author: windows-sdk-content
description: Retrieves the enable/disable settings for the DHCPv4 server's allow/deny lists.
old-location: dhcp\dhcpgetfilterv4.htm
old-project: DHCP
ms.assetid: 2acee985-48b1-4a76-9ca1-2fc27d990032
ms.author: windowssdkdev
ms.date: 05/17/2018
ms.keywords: DhcpGetFilterV4, DhcpGetFilterV4 function [DHCP], dhcp.dhcpgetfilterv4, dhcpsapi/DhcpGetFilterV4
ms.prod: windows
ms.technology: windows-sdk
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
 - DhcpGetFilterV4
product: Windows
targetos: Windows
req.lib: Dhcpsapi.lib
req.dll: Dhcpsapi.dll
req.irql: 
---

# DhcpGetFilterV4 function


## -description


The <b>DhcpGetFilterV4</b> function retrieves the enable/disable settings for the DHCPv4 server's allow/deny lists.


## -parameters




### -param ServerIpAddress [in]

Unicode string that specifies the IP address or hostname of the DHCP server.


### -param GlobalFilterInfo [out]

Pointer to a <a href="https://msdn.microsoft.com/babf9cdb-bd43-41ea-9cb4-209ff129b0f2">DHCP_FILTER_GLOBAL_INFO</a> structure that contains the enable/disable settings for the DHCPv6 server's allow/deny lists.


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
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
This call was performed by a client who is not a member of the "DHCP Administrators" security group.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DHCP_JET_ERROR</b></dt>
</dl>
</td>
<td width="60%">
An error occurred while accessing the DHCP server's database.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/babf9cdb-bd43-41ea-9cb4-209ff129b0f2">DHCP_FILTER_GLOBAL_INFO</a>
 

 

