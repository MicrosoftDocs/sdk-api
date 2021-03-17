---
UID: NF:dhcpsapi.DhcpV4FailoverGetAddressStatus
title: DhcpV4FailoverGetAddressStatus function (dhcpsapi.h)
description: Returns the status of a IPv4 address.
helpviewer_keywords: ["DhcpV4FailoverGetAddressStatus","DhcpV4FailoverGetAddressStatus function [DHCP]","dhcp.dhcpv4failovergetaddressstatus","dhcpsapi/DhcpV4FailoverGetAddressStatus"]
old-location: dhcp\dhcpv4failovergetaddressstatus.htm
tech.root: DHCP
ms.assetid: 4d8371f2-1dc5-487d-b4c0-c5a2071466b2
ms.date: 12/05/2018
ms.keywords: DhcpV4FailoverGetAddressStatus, DhcpV4FailoverGetAddressStatus function [DHCP], dhcp.dhcpv4failovergetaddressstatus, dhcpsapi/DhcpV4FailoverGetAddressStatus
req.header: dhcpsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - DhcpV4FailoverGetAddressStatus
 - dhcpsapi/DhcpV4FailoverGetAddressStatus
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
 - DhcpV4FailoverGetAddressStatus
---

# DhcpV4FailoverGetAddressStatus function


## -description

The <b>DhcpV4FailoverGetAddressStatus</b> function returns the status of a IPv4 address.

## -parameters

### -param ServerIpAddress [in, optional]

Pointer to a null-terminated Unicode string that represents the IP address or hostname of the DHCP server.

### -param SubnetAddress [in]

<a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-type-definitions">DHCP_IP_ADDRESS</a> structure that contains the IPv4 address whose status is being requested.

### -param pStatus [in, out]

Pointer to a DWORD that returns the status of the IPv4 address as specified in the table below:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The IPv4 address will be leased by a primary server.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The IPv4 address will be leased by a secondary server.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The IPv4 address is part of an exclusion range.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>3</dt>
</dl>
</td>
<td width="60%">
The IPv4 address is a reservation.

</td>
</tr>
</table>

## -returns

If the function succeeds, it returns <b>ERROR_SUCCESS</b>.

If the function fails, it returns one of the following or an error code from <a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-api-error-codes">DHCP Server Management API Error Codes</a>.