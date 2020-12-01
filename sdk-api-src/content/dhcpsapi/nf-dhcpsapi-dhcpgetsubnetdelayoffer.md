---
UID: NF:dhcpsapi.DhcpGetSubnetDelayOffer
title: DhcpGetSubnetDelayOffer function (dhcpsapi.h)
description: Obtains the delay period for DHCP OFFER messages after a DISCOVER message is received.
helpviewer_keywords: ["DhcpGetSubnetDelayOffer","DhcpGetSubnetDelayOffer function [DHCP]","dhcp.dhcpgetsubnetdelayoffer","dhcpsapi/DhcpGetSubnetDelayOffer"]
old-location: dhcp\dhcpgetsubnetdelayoffer.htm
tech.root: DHCP
ms.assetid: fce1b0e8-d41c-45f7-99df-4233e76b2597
ms.date: 12/05/2018
ms.keywords: DhcpGetSubnetDelayOffer, DhcpGetSubnetDelayOffer function [DHCP], dhcp.dhcpgetsubnetdelayoffer, dhcpsapi/DhcpGetSubnetDelayOffer
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
 - DhcpGetSubnetDelayOffer
 - dhcpsapi/DhcpGetSubnetDelayOffer
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
 - DhcpGetSubnetDelayOffer
---

# DhcpGetSubnetDelayOffer function


## -description

The <b>DhcpGetSubnetDelayOffer</b> function obtains the delay period for DHCP OFFER messages after a DISCOVER message is received.

## -parameters

### -param ServerIpAddress [in]

Unicode string that specifies the IP address or hostname of the DHCP server.

### -param SubnetAddress [in]

<a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-type-definitions">DHCP_IP_ADDRESS</a> value that contains the IP address of the subnet gateway.

### -param TimeDelayInMilliseconds [out]

Unsigned 16-bit integer value that receive the time to delay an OFFER message after receiving a DISCOVER message as configured on the DHCP server, in milliseconds.

<div class="alert"><b>Note</b>  <p class="note">The memory for this parameter must be free using <a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcprpcfreememory">DhcpRpcFreeMemory</a>.

</div>
<div> </div>

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
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One of the parameters provides an invalid value.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpsetsubnetdelayoffer">DhcpSetSubnetDelayOffer</a>