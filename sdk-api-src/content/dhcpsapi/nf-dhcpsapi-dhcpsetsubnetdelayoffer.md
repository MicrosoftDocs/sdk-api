---
UID: NF:dhcpsapi.DhcpSetSubnetDelayOffer
title: DhcpSetSubnetDelayOffer function (dhcpsapi.h)
description: Sets the delay period for DHCP OFFER messages after a DISCOVER message is received, for a specific DHCP scope.
helpviewer_keywords: ["DhcpSetSubnetDelayOffer","DhcpSetSubnetDelayOffer function [DHCP]","dhcp.dhcpsetsubnetdelayoffer","dhcpsapi/DhcpSetSubnetDelayOffer"]
old-location: dhcp\dhcpsetsubnetdelayoffer.htm
tech.root: DHCP
ms.assetid: f58ba3da-a6c2-48a5-b744-edd9581610f1
ms.date: 12/05/2018
ms.keywords: DhcpSetSubnetDelayOffer, DhcpSetSubnetDelayOffer function [DHCP], dhcp.dhcpsetsubnetdelayoffer, dhcpsapi/DhcpSetSubnetDelayOffer
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DhcpSetSubnetDelayOffer
 - dhcpsapi/DhcpSetSubnetDelayOffer
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Dhcpsapi.dll
api_name:
 - DhcpSetSubnetDelayOffer
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

This function returns <b>ERROR_SUCCESS</b> upon a successful call. Otherwise, it returns one of the <a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-api-error-codes">DHCP Server Management API Error Codes</a>.

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

<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpgetsubnetdelayoffer">DhcpGetSubnetDelayOffer</a>