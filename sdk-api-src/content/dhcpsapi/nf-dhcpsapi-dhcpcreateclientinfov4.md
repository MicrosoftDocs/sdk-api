---
UID: NF:dhcpsapi.DhcpCreateClientInfoV4
title: DhcpCreateClientInfoV4 function (dhcpsapi.h)
author: windows-sdk-content
description: Creates a client information record on the DHCP server, extending the functionality of DhcpCreateClientInfo by including the client type (DHCP or BOOTP) in the record.
old-location: dhcp\dhcpcreateclientinfov4.htm
tech.root: DHCP
ms.assetid: 0657e107-bf3d-4bcd-88a1-84a6cd7f934d
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DhcpCreateClientInfoV4, DhcpCreateClientInfoV4 function [DHCP], dhcp.dhcpcreateclientinfov4, dhcpsapi/DhcpCreateClientInfoV4
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
 - DhcpCreateClientInfoV4
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DhcpCreateClientInfoV4 function


## -description


The <b>DhcpCreateClientInfoV4</b> function creates a client information record on the DHCP server, extending the functionality of <a href="https://msdn.microsoft.com/121718db-a7d8-42b7-b1a1-5c2dbe7d3d6b">DhcpCreateClientInfo</a> by including the client type (DHCP or BOOTP) in the record.


## -parameters




### -param ServerIpAddress [in]

Unicode string that specifies the IP address or hostname of the DHCP server.


### -param ClientInfo [in]

Pointer to a <a href="https://msdn.microsoft.com/ac058d7a-7257-4e40-8fc0-bc4ca107671b">DHCP_CLIENT_INFO_V4</a> structure that contains information about the DHCP client, including the assigned IP address, the subnet mask, the  host, and the client type (DHCP and/or BOOTP).


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
</table>
 




## -remarks



When successful, a call to this additionally marks the specified DHCP client IPv4 address as unavailable, in order to avoid IP duplication.




## -see-also




<a href="https://msdn.microsoft.com/ac058d7a-7257-4e40-8fc0-bc4ca107671b">DHCP_CLIENT_INFO_V4</a>



<a href="https://msdn.microsoft.com/121718db-a7d8-42b7-b1a1-5c2dbe7d3d6b">DhcpCreateClientInfo</a>
 

 

