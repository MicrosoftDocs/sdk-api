---
UID: NF:dhcpsapi.DhcpAddSubnetElementV6
title: DhcpAddSubnetElementV6 function (dhcpsapi.h)
author: windows-sdk-content
description: The DhcpAddSubnetElementV6 function adds an element describing a feature or aspect of the subnet to the subnet entry in the DHCP database.
old-location: dhcp\dhcpaddsubnetelementv6.htm
tech.root: DHCP
ms.assetid: 9f009140-5301-4aee-a6e5-12f7cd56f906
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DhcpAddSubnetElementV6, DhcpAddSubnetElementV6 function [DHCP], dhcp.dhcpaddsubnetelementv6, dhcpsapi/DhcpAddSubnetElementV6
ms.topic: function
req.header: dhcpsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - DhcpAddSubnetElementV6
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DhcpAddSubnetElementV6 function


## -description


The <b>DhcpAddSubnetElementV6</b> function  adds an element describing a feature or aspect of the subnet to the subnet entry in the DHCP database. 


## -parameters




### -param ServerIpAddress [in]

Pointer to a Unicode string that specifies the IP address or hostname of the DHCP server.


### -param SubnetAddress [in]

DHCP_IPV6_ADDRESS structure that contains the IP address of the subnet.


### -param AddElementInfo [in]

Pointer to a DHCP_SUBNET_ELEMENT_DATA_V6 structure that contains the element data to add to the subnet. The V5 structure adds support for BOOTP clients.


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
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The parameters were invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DUPLICATE_TAG</b></dt>
</dl>
</td>
<td width="60%">
The specified scope already exists.

</td>
</tr>
</table>
 



