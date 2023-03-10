---
UID: NF:dhcpsapi.DhcpGetAllOptionValues
title: DhcpGetAllOptionValues function (dhcpsapi.h)
description: Returns an array that contains all option values defined for a specific scope on the DHCP server.
helpviewer_keywords: ["DHCP_FLAGS_OPTION_IS_VENDOR","DhcpGetAllOptionValues","DhcpGetAllOptionValues function [DHCP]","dhcp.dhcpgetalloptionvalues","dhcpsapi/DhcpGetAllOptionValues"]
old-location: dhcp\dhcpgetalloptionvalues.htm
tech.root: DHCP
ms.assetid: c462feba-dd9b-4815-b4d4-db1cdec3a354
ms.date: 12/05/2018
ms.keywords: DHCP_FLAGS_OPTION_IS_VENDOR, DhcpGetAllOptionValues, DhcpGetAllOptionValues function [DHCP], dhcp.dhcpgetalloptionvalues, dhcpsapi/DhcpGetAllOptionValues
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
 - DhcpGetAllOptionValues
 - dhcpsapi/DhcpGetAllOptionValues
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
 - DhcpGetAllOptionValues
---

# DhcpGetAllOptionValues function


## -description

The <b>DhcpGetAllOptionValues</b> function returns an array that contains all option values defined for a specific scope on the DHCP server.

## -parameters

### -param ServerIpAddress [in]

Unicode string that specifies the IP address or hostname of the DHCP server.

### -param Flags [in]

Specifies a bit flag that indicates whether the options are vendor-specific. If the qualification of vendor options is not necessary, this parameter should be 0.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DHCP_FLAGS_OPTION_IS_VENDOR"></a><a id="dhcp_flags_option_is_vendor"></a><dl>
<dt><b>DHCP_FLAGS_OPTION_IS_VENDOR</b></dt>
</dl>
</td>
<td width="60%">
This flag should be set if vendor-specific options are desired.

</td>
</tr>
</table>

### -param ScopeInfo [in]

Pointer to a <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_option_scope_info">DHCP_OPTION_SCOPE_INFO</a> structure that contains information on the specific scope whose option values will be returned. This information defines the option values that are being retrieved from the default, server, or scope level, or for a specific IPv4 reservation.

### -param Values [out]

Pointer to a <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_all_option_values">DHCP_ALL_OPTION_VALUES</a> structure that contains the returned option values for the scope specified in <i>ScopeInfo</i>.

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
This specified IPv4 sunet is not defined on the DHCP server.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DHCP_NOT_RESERVED_CLIENT</b></dt>
</dl>
</td>
<td width="60%">
The specified DHCP client is not a reserved client.

</td>
</tr>
</table>

## -remarks

There will be one option value in the array specified by <i>Values</i> for each vendor/class pair defined on the DHCP server.

## -see-also

<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpgetalloptions">DhcpGetAllOptions</a>