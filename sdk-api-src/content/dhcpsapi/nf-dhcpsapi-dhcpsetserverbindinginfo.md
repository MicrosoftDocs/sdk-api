---
UID: NF:dhcpsapi.DhcpSetServerBindingInfo
title: DhcpSetServerBindingInfo function (dhcpsapi.h)
description: The DhcpSetServerBindingInfo function sets endpoint bindings for the DHCP server.
helpviewer_keywords: ["DHCP_ENDPOINT_FLAG_CANT_MODIFY","DhcpSetServerBindingInfo","DhcpSetServerBindingInfo function [DHCP]","dhcp.dhcpsetserverbindinginfo","dhcpsapi/DhcpSetServerBindingInfo"]
old-location: dhcp\dhcpsetserverbindinginfo.htm
tech.root: DHCP
ms.assetid: 6291e266-e9d5-4899-8b34-53695f49a1b8
ms.date: 12/05/2018
ms.keywords: DHCP_ENDPOINT_FLAG_CANT_MODIFY, DhcpSetServerBindingInfo, DhcpSetServerBindingInfo function [DHCP], dhcp.dhcpsetserverbindinginfo, dhcpsapi/DhcpSetServerBindingInfo
req.header: dhcpsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - DhcpSetServerBindingInfo
 - dhcpsapi/DhcpSetServerBindingInfo
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
 - DhcpSetServerBindingInfo
---

# DhcpSetServerBindingInfo function


## -description

The <b>DhcpSetServerBindingInfo</b> function sets endpoint bindings for the DHCP server.

## -parameters

### -param ServerIpAddress [in]

Unicode string that specifies the IP address or hostname of the DHCP server.

### -param Flags [in]

Specifies a set of flags describing endpoint properties.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DHCP_ENDPOINT_FLAG_CANT_MODIFY"></a><a id="dhcp_endpoint_flag_cant_modify"></a><dl>
<dt><b>DHCP_ENDPOINT_FLAG_CANT_MODIFY</b></dt>
<dt>0x01</dt>
</dl>
</td>
<td width="60%">
The endpoints cannot be modified.

</td>
</tr>
</table>

### -param BindElementInfo [in]

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_bind_element_array">DHCP_BIND_ELEMENT_ARRAY</a> structure that contains the endpoint bindings for the DHCP server.

## -returns

This function returns <b>ERROR_SUCCESS</b> upon a successful call. Otherwise, it returns one of the <a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-api-error-codes">DHCP Server Management API Error Codes</a>.

## -remarks

This function requires network byte ordering for all <a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-type-definitions">DHCP_IP_ADDRESS</a> values in parameter structures.

## -see-also

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_bind_element_array">DHCP_BIND_ELEMENT_ARRAY</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpgetserverbindinginfo">DhcpGetServerBindingInfo</a>