---
UID: NF:dhcpsapi.DhcpV4GetAllOptionValues
title: DhcpV4GetAllOptionValues function (dhcpsapi.h)
description: Retrieves an array of DHCP option values (the option code and associated data) for a particular scope.
helpviewer_keywords: ["DHCP_FLAGS_OPTION_IS_VENDOR","DhcpV4GetAllOptionValues","DhcpV4GetAllOptionValues function [DHCP]","dhcp.dhcpv4getalloptionvalues","dhcpsapi/DhcpV4GetAllOptionValues"]
old-location: dhcp\dhcpv4getalloptionvalues.htm
tech.root: DHCP
ms.assetid: 3c2fff2f-3d79-4e0d-8a31-9917088b1413
ms.date: 12/05/2018
ms.keywords: DHCP_FLAGS_OPTION_IS_VENDOR, DhcpV4GetAllOptionValues, DhcpV4GetAllOptionValues function [DHCP], dhcp.dhcpv4getalloptionvalues, dhcpsapi/DhcpV4GetAllOptionValues
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
 - DhcpV4GetAllOptionValues
 - dhcpsapi/DhcpV4GetAllOptionValues
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
 - DhcpV4GetAllOptionValues
---

# DhcpV4GetAllOptionValues function


## -description

The <b>DhcpV4GetAllOptionValues</b> function retrieves an array of DHCP option values (the option code and associated data) for a particular scope.

## -parameters

### -param ServerIpAddress [in, optional]

Pointer to a null-terminated Unicode string that represents the IP address or hostname of the DHCP server.

### -param Flags [in]

Indicates whether the option values are for a specific or default vendor.

<table>
<tr>
<th>Flags</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>0x00000000</dt>
</dl>
</td>
<td width="60%">
The option values are retrieved for a default vendor.

</td>
</tr>
<tr>
<td width="40%"><a id="DHCP_FLAGS_OPTION_IS_VENDOR"></a><a id="dhcp_flags_option_is_vendor"></a><dl>
<dt><b>DHCP_FLAGS_OPTION_IS_VENDOR</b></dt>
<dt>0x00000003</dt>
</dl>
</td>
<td width="60%">
The option values are retrieved for specific vendors.

</td>
</tr>
</table>

### -param ScopeInfo [in]

A pointer to a <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_option_scope_info">DHCP_OPTION_SCOPE_INFO</a> structure that contains information on the scope of the option values to retrieve.

### -param Values [out]

Pointer to a <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_all_option_values_pb">DHCP_ALL_OPTION_VALUES_PB</a> structure that contains the retrieved option values for the scope specified in <i>ScopeInfo</i>.

There is one option value in the array for each vendor/policy pair defined on the DHCP server.

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
</table>

## -remarks

<i>Values</i> should be free using <a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcprpcfreememory">DhcpRpcFreeMemory</a>.

## -see-also

<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpv4getoptionvalue">DhcpV4GetOptionValue</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpv4removeoptionvalue">DhcpV4RemoveOptionValue</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpv4setoptionvalue">DhcpV4SetOptionValue</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpv4setoptionvalues">DhcpV4SetOptionValues</a>