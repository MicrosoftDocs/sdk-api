---
UID: NF:dhcpsapi.DhcpV4EnumSubnetReservations
title: DhcpV4EnumSubnetReservations function (dhcpsapi.h)
description: Enumerates the reservations for a specific DHCP IPv4 subnet.
helpviewer_keywords: ["DhcpV4EnumSubnetReservations","DhcpV4EnumSubnetReservations function [DHCP]","dhcp.dhcpv4enumsubnetreservations","dhcpsapi/DhcpV4EnumSubnetReservations"]
old-location: dhcp\dhcpv4enumsubnetreservations.htm
tech.root: DHCP
ms.assetid: 6eebc858-7ffe-4bf3-b318-3a5ad16c9827
ms.date: 12/05/2018
ms.keywords: DhcpV4EnumSubnetReservations, DhcpV4EnumSubnetReservations function [DHCP], dhcp.dhcpv4enumsubnetreservations, dhcpsapi/DhcpV4EnumSubnetReservations
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
 - DhcpV4EnumSubnetReservations
 - dhcpsapi/DhcpV4EnumSubnetReservations
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
 - DhcpV4EnumSubnetReservations
---

# DhcpV4EnumSubnetReservations function


## -description

The <b>DhcpV4EnumSubnetReservations</b> function enumerates the reservations for a specific DHCP IPv4 subnet.

## -parameters

### -param ServerIpAddress [in, optional]

Pointer to a null-terminated Unicode string that represents the IP address or hostname of the DHCP server.

### -param SubnetAddress [in]

<a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-type-definitions">DHCP_IP_ADDRESS</a> structure that contains the IPv4 subnet address of the reservations to enumerate.

### -param ResumeHandle [in, out]

Pointer to a  <a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-type-definitions">DHCP_RESUME_HANDLE</a> structure that identifies this enumeration for use in subsequent calls to this function.

Initially, this value should be zero on input. If successful, the returned value should be used for subsequent enumeration requests. For example, if <i>PreferredMaximum</i> is set to 100, and 200 reservation elements are configured on the server, the resume handle can be used after the first 100 policies are retrieved to obtain the next 100 on a subsequent call.

### -param PreferredMaximum [in]

 The maximum number of bytes of subnet reservations to return in <i>EnumInfo</i>. If <i>PreferredMaximum</i> is greater than the number of remaining non-enumerated bytes of subnet reservations on the server, the remaining number of  non-enumerated bytes is returned. To retrieve all the subnet reservation elements, set this parameter to 0xFFFFFFFF.

### -param EnumElementInfo [out]

Pointer to a <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_reservation_info_array">DHCP_RESERVATION_INFO_ARRAY</a> structure that contains the reservations elements available for the specified subnet. If no elements are configured, this value is <b>NULL</b>.

### -param ElementsRead [out]

Pointer to a <b>DWORD</b> that specifies the number of reservation elements returned in <i>EnumElementInfo</i>.

### -param ElementsTotal [out]

Pointer to a <b>DWORD</b>  that specifies the number of reservations on the DHCP server that have not yet been enumerated.

## -returns

If the function succeeds, it returns <b>ERROR_SUCCESS</b>.

If the function fails, it returns one of the following or an error code from <a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-api-error-codes">DHCP Server Management API Error Codes</a>.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One or more of the parameters were invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
There are more elements available to enumerate.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_MORE_ITEMS</b></dt>
</dl>
</td>
<td width="60%">
There are no more elements left to enumerate.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DHCP_SUBNET_NOT_PRESENT</b></dt>
</dl>
</td>
<td width="60%">
IPv4 subnet does not exist on the DHCPv4 server.

</td>
</tr>
</table>

## -remarks

<i>EnumElementInfo</i> should be free using <a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcprpcfreememory">DhcpRpcFreeMemory</a>.