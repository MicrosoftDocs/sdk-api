---
UID: NF:dhcpsapi.DhcpGetAllOptions
title: DhcpGetAllOptions function (dhcpsapi.h)
description: Returns an array that contains all options defined on the DHCP server.
helpviewer_keywords: ["DHCP_FLAGS_OPTION_IS_VENDOR","DhcpGetAllOptions","DhcpGetAllOptions function [DHCP]","dhcp.dhcpgetalloptions","dhcpsapi/DhcpGetAllOptions"]
old-location: dhcp\dhcpgetalloptions.htm
tech.root: DHCP
ms.assetid: 72284a0e-4bd9-451a-bf6b-4b11bbbd4511
ms.date: 12/05/2018
ms.keywords: DHCP_FLAGS_OPTION_IS_VENDOR, DhcpGetAllOptions, DhcpGetAllOptions function [DHCP], dhcp.dhcpgetalloptions, dhcpsapi/DhcpGetAllOptions
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
 - DhcpGetAllOptions
 - dhcpsapi/DhcpGetAllOptions
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
 - DhcpGetAllOptions
---

# DhcpGetAllOptions function


## -description

The <b>DhcpGetAllOptions</b> function returns an array that contains all options defined on the DHCP server.

## -parameters

### -param ServerIpAddress [in]

Unicode string that specifies the IP address or hostname of the DHCP server.

### -param Flags [in]

Specifies a bit flag that indicates whether or not the options are vendor-specific. If the qualification of vendor options is not necessary, this parameter should be 0.

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

### -param OptionStruct [out]

Pointer to a <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_all_options">DHCP_ALL_OPTIONS</a> structure containing every option defined for a vendor or default class. If there are no options available on the server, this value will be null.

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
<dt><b>ERROR_DHCP_JET_ERROR</b></dt>
</dl>
</td>
<td width="60%">
An error occurred while accessing the DHCP server database.

</td>
</tr>
</table>

## -remarks

There will be one option element in the array specified by <i>OptionStruct</i> for each vendor/class pair defined on the DHCP server.

## -see-also

<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpgetalloptionvalues">DhcpGetAllOptionValues</a>