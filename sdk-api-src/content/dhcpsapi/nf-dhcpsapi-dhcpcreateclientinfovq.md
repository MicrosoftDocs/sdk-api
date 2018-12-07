---
UID: NF:dhcpsapi.DhcpCreateClientInfoVQ
title: DhcpCreateClientInfoVQ function
author: windows-sdk-content
description: Creates the provided DHCP client lease record in the DHCP server database.
old-location: dhcp\dhcpcreateclientinfovq.htm
tech.root: DHCP
ms.assetid: 8b47bd52-e153-4000-9f4e-5335f029464b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DhcpCreateClientInfoVQ, DhcpCreateClientInfoVQ function [DHCP], dhcp.dhcpcreateclientinfovq, dhcpsapi/DhcpCreateClientInfoVQ
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - DhcpCreateClientInfoVQ
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DhcpCreateClientInfoVQ function


## -description


The <b>DhcpCreateClientInfoVQ</b> function creates the provided DHCP client lease record in the DHCP server database.


## -parameters




### -param ServerIpAddress [in]

Unicode string that specifies the IP address or hostname of the DHCP server.


### -param ClientInfo [in]

Pointer to a <a href="https://msdn.microsoft.com/f7bd832d-b4a4-404c-8959-e9653b62d434">DHCP_CLIENT_INFO_VQ</a> structure that contains the DHCP client lease record information to set on the DHCP server. The caller must populate the <b>ClientIPAddress</b> and <b>ClientHardwareAddress</b> fields of this structure; all others are optional.


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



Additionally, this API marks the specified client IP address as unavailable (or distributed) to avoid IP collisions. 




## -see-also




<a href="https://msdn.microsoft.com/c12ae8f5-8629-494f-905c-cbae57dcf3f1">DhcpSetClientInfoVQ</a>
 

 

