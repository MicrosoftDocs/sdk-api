---
UID: NF:dhcpsapi.DhcpSetClientInfoV4
title: DhcpSetClientInfoV4 function
author: windows-sdk-content
description: Sets information on a client whose IP address lease is administrated by the DHCP server. This function extends the functionality provided by DhcpSetClientInfo by allowing the caller to specify the client type (DHCP or BOOTP).
old-location: dhcp\dhcpsetclientinfov4.htm
old-project: DHCP
ms.assetid: f7e1aa86-634e-48a7-ae2a-9c23277ed946
ms.author: windowssdkdev
ms.date: 05/17/2018
ms.keywords: DhcpSetClientInfoV4, DhcpSetClientInfoV4 function [DHCP], dhcp.dhcpsetclientinfov4, dhcpsapi/DhcpSetClientInfoV4
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
-	DhcpSetClientInfoV4
product: Windows
targetos: Windows
req.lib: Dhcpsapi.lib
req.dll: Dhcpsapi.dll
req.irql: 
---

# DhcpSetClientInfoV4 function


## -description


The <b>DhcpSetClientInfoV4</b> function sets information on a client whose IP address lease is administrated by the DHCP server. This function extends the functionality provided by <a href="https://msdn.microsoft.com/1eedddce-8b3e-419e-a065-163b22a0e9a8">DhcpSetClientInfo</a> by allowing the caller to specify the client type (DHCP or BOOTP).


## -parameters




### -param ServerIpAddress [in]

Unicode string that specifies the IP address or hostname of the DHCP server.


### -param ClientInfo [in]

Pointer to a <a href="https://msdn.microsoft.com/ac058d7a-7257-4e40-8fc0-bc4ca107671b">DHCP_CLIENT_INFO_V4</a> structure that contains the information, including client type, for a client in a subnet served by the DHCP server.


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




<a href="https://msdn.microsoft.com/ac058d7a-7257-4e40-8fc0-bc4ca107671b">DHCP_CLIENT_INFO_V4</a>



<a href="https://msdn.microsoft.com/67095868-7e02-4d82-b2f0-70c413fa8ed6">DhcpGetClientInfoV4</a>



<a href="https://msdn.microsoft.com/1eedddce-8b3e-419e-a065-163b22a0e9a8">DhcpSetClientInfo</a>
 

 

