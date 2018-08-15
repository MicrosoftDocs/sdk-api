---
UID: NF:dhcpsapi.DhcpSetSubnetDelayOffer
title: DhcpSetSubnetDelayOffer function
author: windows-sdk-content
description: Sets the delay period for DHCP OFFER messages after a DISCOVER message is received, for a specific DHCP scope.
old-location: dhcp\dhcpsetsubnetdelayoffer.htm
old-project: dhcp
ms.assetid: f58ba3da-a6c2-48a5-b744-edd9581610f1
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: DhcpSetSubnetDelayOffer, DhcpSetSubnetDelayOffer function [DHCP], dhcp.dhcpsetsubnetdelayoffer, dhcpsapi/DhcpSetSubnetDelayOffer
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: dhcpsapi.h
req.include-header: 
req.redist: 
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
 - DhcpSetSubnetDelayOffer
product: Windows
targetos: Windows
req.lib: Dhcpsapi.lib
req.dll: Dhcpsapi.dll
req.irql: 
---

# DhcpSetSubnetDelayOffer function


## -description


The <b>DhcpSetSubnetDelayOffer</b> function sets the delay period for DHCP OFFER messages after a DISCOVER message is received, for a specific DHCP scope.


## -parameters




### -param ServerIpAddress [in]

Unicode string that specifies the IP address or hostname of the DHCP server.


### -param SubnetAddress [in]

<b>DHCP_IP_ADDRESS</b> value that contains the IP address of the subnet gateway.


### -param TimeDelayInMilliseconds [in]

Unsigned 16-bit integer value that specifies the time to delay an OFFER message after receiving a DISCOVER message, in milliseconds, and set for a particular scope. This value must be between 0 and 1000 (milliseconds). The default value is 0.


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
<dt><b>ERROR_DHCP_SUBNET_NOT_PRESENT</b></dt>
</dl>
</td>
<td width="60%">
The specified subnet is not defined on the DHCP server.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DHCP_INVALID_DELAY</b></dt>
</dl>
</td>
<td width="60%">
The time delay was set to a value less than 0 or greater than 1000.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One of the parameters provides an invalid value.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/fce1b0e8-d41c-45f7-99df-4233e76b2597">DhcpGetSubnetDelayOffer</a>
 

 

