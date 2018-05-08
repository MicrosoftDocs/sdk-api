---
UID: NF:dhcpsapi.DhcpCreateOption
title: DhcpCreateOption function
author: windows-driver-content
description: Creates an option definition for the default user and vendor class at the default option level.
old-location: dhcp\dhcpcreateoption.htm
old-project: DHCP
ms.assetid: 2a77467e-12e8-4a8e-a6ab-e3783a7492da
ms.author: windowsdriverdev
ms.date: 5/2/2018
ms.keywords: DhcpCreateOption, DhcpCreateOption function [DHCP], dhcp.dhcpcreateoption, dhcpsapi/DhcpCreateOption
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
req.typenames: QuarantineStatus
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Dhcpsapi.dll
api_name:
-	DhcpCreateOption
product: Windows
targetos: Windows
req.lib: Dhcpsapi.lib
req.dll: Dhcpsapi.dll
req.irql: 
---

# DhcpCreateOption function


## -description


The <b>DhcpCreateOption</b> function creates an option definition for the default user and vendor class at the default option level.


## -parameters




### -param ServerIpAddress [in]

Unicode string containing the IPv4 address of the DHCP server.


### -param OptionID [in]


<a href="https://msdn.microsoft.com/8e29f488-2978-43dd-b7ba-edad2e3e4b29">DHCP_OPTION_ID</a> value that contains the unique option ID number (also called an "option code") of the new option. Many of these option ID numbers are defined; a complete list of standard DHCP and BOOTP option codes can be found in  <a href="http://go.microsoft.com/fwlink/p/?linkid=84033">DHCP Options and BOOTP Vendor Extensions</a>.


### -param OptionInfo [in]


<a href="https://msdn.microsoft.com/1be34eb4-a226-4f07-b763-173a4f8a0671">DHCP_OPTION</a> structure that contains information describing the new   DHCP option, including the name, an optional comment, and any related data items.


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
<dt><b>ERROR_DHCP_JET_ERROR</b></dt>
</dl>
</td>
<td width="60%">
An error occurred while accessing the DHCP server database.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DHCP_OPTION_EXISTS</b></dt>
</dl>
</td>
<td width="60%">
The specified option definition already exists in the DHCP server database.

</td>
</tr>
</table>
 




## -remarks



An option is a client configuration parameter assigned by a DHCP server to DHCP and BOOTP clients. For example, some commonly used options include IP addresses for gateways (subnet routers), WINS servers, and DNS servers. Typically, these options are enabled and configured for a particular scope, but default options can be created for all scopes served by a given DHCP server.




## -see-also




<a href="https://msdn.microsoft.com/8e29f488-2978-43dd-b7ba-edad2e3e4b29">DHCP_OPTION_ID</a>



<a href="https://msdn.microsoft.com/de6e8f87-af4b-4e7f-8468-54359c5a8907">DhcpCreateOptionV5</a>
 

 

