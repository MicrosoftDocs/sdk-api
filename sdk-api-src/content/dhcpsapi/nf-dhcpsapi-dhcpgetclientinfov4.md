---
UID: NF:dhcpsapi.DhcpGetClientInfoV4
title: DhcpGetClientInfoV4 function
author: windows-sdk-content
description: Returns information on a specific DHCP client. This function extends DhcpGetClientInfo by returning a DHCP_CLIENT_INFO_V4 structure that contains client type information.
old-location: dhcp\dhcpgetclientinfov4.htm
old-project: DHCP
ms.assetid: 3f8b9cbb-f903-4a97-8a38-caf2210b6d48
ms.author: windowssdkdev
ms.date: 05/17/2018
ms.keywords: DhcpGetClientInfoV4, DhcpGetClientInfoV4 function [DHCP], dhcp.dhcpgetclientinfov4, dhcpsapi/DhcpGetClientInfoV4
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
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Dhcpsapi.dll
api_name:
-	DhcpGetClientInfoV4
product: Windows
targetos: Windows
req.lib: Dhcpsapi.lib
req.dll: Dhcpsapi.dll
req.irql: 
---

# DhcpGetClientInfoV4 function


## -description


The <b>DhcpGetClientInfoV4</b> function returns information on a specific DHCP client. This function extends <a href="https://msdn.microsoft.com/67095868-7e02-4d82-b2f0-70c413fa8ed6">DhcpGetClientInfo</a> by returning a <a href="https://msdn.microsoft.com/ac058d7a-7257-4e40-8fc0-bc4ca107671b">DHCP_CLIENT_INFO_V4</a> structure that contains client type information.


## -parameters




### -param ServerIpAddress [in]

Specifies the IP address of the DHCP server.


### -param SearchInfo [in]


<a href="https://msdn.microsoft.com/3c6f85d7-c156-4379-bad9-0705698f12e5">DHCP_SEARCH_INFO</a> structure that contains the search parameters used to select a specific DHCP client.


### -param ClientInfo [out]


<a href="https://msdn.microsoft.com/ac058d7a-7257-4e40-8fc0-bc4ca107671b">DHCP_CLIENT_INFO_V4</a> structure that contains information that describes the DHCP client that most closely matches the provided search parameters. If no client could be found, this parameter will be null.

<div class="alert"><b>Note</b>  <p class="note">The memory for this parameter must be free using <a href="https://msdn.microsoft.com/bf22a0a6-2ecd-4460-89c4-3f870c6275dc">DhcpRpcFreeMemory</a>.

</div>
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




<a href="https://msdn.microsoft.com/ac058d7a-7257-4e40-8fc0-bc4ca107671b">
		  DHCP_CLIENT_INFO_V4</a>



<a href="https://msdn.microsoft.com/3c6f85d7-c156-4379-bad9-0705698f12e5">DHCP_SEARCH_INFO</a>



<a href="https://msdn.microsoft.com/67095868-7e02-4d82-b2f0-70c413fa8ed6">DhcpGetClientInfo</a>



<a href="https://msdn.microsoft.com/1eedddce-8b3e-419e-a065-163b22a0e9a8">DhcpSetClientInfo</a>
 

 

