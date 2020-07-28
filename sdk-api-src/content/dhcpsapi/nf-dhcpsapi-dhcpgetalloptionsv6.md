---
UID: NF:dhcpsapi.DhcpGetAllOptionsV6
title: DhcpGetAllOptionsV6 function (dhcpsapi.h)
description: The DhcpGetAllOptionsV6 function returns an array that contains all options defined on the DHCP server.
helpviewer_keywords: ["DHCP_FLAGS_OPTION_IS_VENDOR","DhcpGetAllOptionsV6","DhcpGetAllOptionsV6 function [DHCP]","dhcp.dhcpgetalloptionsv6","dhcpsapi/DhcpGetAllOptionsV6"]
old-location: dhcp\dhcpgetalloptionsv6.htm
tech.root: DHCP
ms.assetid: 66a49f05-66ab-489d-abd7-b9f0bbe5a7cc
ms.date: 12/05/2018
ms.keywords: DHCP_FLAGS_OPTION_IS_VENDOR, DhcpGetAllOptionsV6, DhcpGetAllOptionsV6 function [DHCP], dhcp.dhcpgetalloptionsv6, dhcpsapi/DhcpGetAllOptionsV6
f1_keywords:
- dhcpsapi/DhcpGetAllOptionsV6
dev_langs:
- c++
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
- DhcpGetAllOptionsV6
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DhcpGetAllOptionsV6 function


## -description


The <b>DhcpGetAllOptionsV6</b> function returns an array that contains all options defined on the DHCP server.


## -parameters




### -param ServerIpAddress [in]

Pointer to a Unicode string that specifies the IP address or hostname of the DHCP server.


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

Pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_all_options">DHCP_ALL_OPTIONS</a> structure containing every option defined on the DHCP server. If there are no options available on the server, this value will be null.

<div class="alert"><b>Note</b>  <p class="note">The memory for this parameter must be free using <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcprpcfreememory">DhcpRpcFreeMemory</a>.

</div>
<div> </div>

## -returns



This function returns <b>ERROR_SUCCESS</b> upon a successful call. Otherwise, it returns one of the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/dhcp/dhcp-server-management-api-error-codes">DHCP Server Management API Error Codes</a>.

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
<dt><b>ERROR_NO_MORE_ITEMS</b></dt>
</dl>
</td>
<td width="60%">
No more items to enumerate.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
Memory failure.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
More data is available to enumerate.

</td>
</tr>
</table>
 



