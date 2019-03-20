---
UID: NF:dhcpsapi.DhcpDeleteClientInfoV6
title: DhcpDeleteClientInfoV6 function (dhcpsapi.h)
author: windows-sdk-content
description: Deletes the specified DHCPv6 client address release record from the DHCPv6 server database.
old-location: dhcp\dhcpdeleteclientinfov6.htm
tech.root: DHCP
ms.assetid: ffa57208-09c4-4185-8cd9-abcf5db60f39
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DhcpDeleteClientInfoV6, DhcpDeleteClientInfoV6 function [DHCP], dhcp.dhcpdeleteclientinfov6, dhcpsapi/DhcpDeleteClientInfoV6
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
 - DhcpDeleteClientInfoV6
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DhcpDeleteClientInfoV6 function


## -description


The <b>DhcpDeleteClientInfoV6</b> function deletes the specified DHCPv6 client address release record from the DHCPv6 server database.


## -parameters




### -param ServerIpAddress [in]

Pointer to a Unicode string that specifies the IP address or hostname of the DHCP server.


### -param ClientInfo [in]

Pointer to a <a href="https://msdn.microsoft.com/b290baab-9a70-437a-a519-876891184fbc">DHCP_SEARCH_INFO_V6</a> structure that contains the key used to search for the DHCPv6 client lease record that will be deleted.


## -returns



This function returns <b>ERROR_SUCCESS</b> upon a successful call. Otherwise, it returns one of the <a href="https://msdn.microsoft.com/6370313f-d7db-4ff1-b0e0-7fa47474facb">DHCP Server Management API Error Codes</a>. Commonly returned error codes include:

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
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DHCP_RESERVEDIP_EXISTS</b></dt>
</dl>
</td>
<td width="60%">
The specified client lease is a reservation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The <b>SearchType</b> member of <a href="https://msdn.microsoft.com/b290baab-9a70-437a-a519-876891184fbc">DHCP_SEARCH_INFO_V6</a> was not set to <b>Dhcpv6ClientIpAddress</b>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/b290baab-9a70-437a-a519-876891184fbc">DHCP_SEARCH_INFO_V6</a>
 

 

