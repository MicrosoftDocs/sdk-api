---
UID: NF:dhcpsapi.DhcpGetClientInfoVQ
title: DhcpGetClientInfoVQ function
author: windows-sdk-content
description: Retrieves DHCP client lease record information from the DHCP server database.
old-location: dhcp\dhcpgetclientinfovq.htm
tech.root: DHCP
ms.assetid: e8ed729b-12c2-4179-b7ef-6c71acf2672e
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DhcpGetClientInfoVQ, DhcpGetClientInfoVQ function [DHCP], dhcp.dhcpgetclientinfovq, dhcpsapi/DhcpGetClientInfoVQ
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
 - DhcpGetClientInfoVQ
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DhcpGetClientInfoVQ function


## -description


The <b>DhcpGetClientInfoVQ</b> function retrieves DHCP client lease record information from the DHCP server database.


## -parameters




### -param ServerIpAddress [in]

Unicode string that specifies the IP address or hostname of the DHCP server.


### -param SearchInfo [in]

Pointer to a <a href="https://msdn.microsoft.com/3c6f85d7-c156-4379-bad9-0705698f12e5">DHCP_SEARCH_INFO</a> structure that defines the key used to search the client lease record database on the DHCP server for a particular client record.


### -param ClientInfo [out]

Pointer to the <a href="https://msdn.microsoft.com/f7bd832d-b4a4-404c-8959-e9653b62d434">DHCP_CLIENT_INFO_VQ</a> structure returned by a successful search operation.


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
 




## -remarks



The caller of this function must release the memory used by the <a href="https://msdn.microsoft.com/f7bd832d-b4a4-404c-8959-e9653b62d434">DHCP_CLIENT_INFO_VQ</a> structure returned in <i>ClientInfo</i>.




## -see-also




<a href="https://msdn.microsoft.com/f7bd832d-b4a4-404c-8959-e9653b62d434">DHCP_CLIENT_INFO_VQ</a>



<a href="https://msdn.microsoft.com/3c6f85d7-c156-4379-bad9-0705698f12e5">DHCP_SEARCH_INFO</a>
 

 

