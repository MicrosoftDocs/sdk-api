---
UID: NF:dhcpsapi.DhcpServerSetConfigVQ
title: DhcpServerSetConfigVQ function (dhcpsapi.h)
description: Sets or updates DHCP server settings.
helpviewer_keywords: ["DhcpServerSetConfigVQ","DhcpServerSetConfigVQ function [DHCP]","dhcp.dhcpserversetconfigvq","dhcpsapi/DhcpServerSetConfigVQ"]
old-location: dhcp\dhcpserversetconfigvq.htm
tech.root: DHCP
ms.assetid: 3498b674-5771-47b6-9dfa-a8e3e10bca40
ms.date: 12/05/2018
ms.keywords: DhcpServerSetConfigVQ, DhcpServerSetConfigVQ function [DHCP], dhcp.dhcpserversetconfigvq, dhcpsapi/DhcpServerSetConfigVQ
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
 - DhcpServerSetConfigVQ
 - dhcpsapi/DhcpServerSetConfigVQ
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
 - DhcpServerSetConfigVQ
---

# DhcpServerSetConfigVQ function


## -description

The <b>DhcpServerSetConfigVQ</b> function sets or updates DHCP server settings.

## -parameters

### -param ServerIpAddress [in]

Unicode string that specifies the IP address or hostname of the DHCP server.

### -param FieldsToSet [in]

Specifies a bitmask of the fields to set in the <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_server_config_info_vq">DHCP_SERVER_CONFIG_INFO_VQ</a> structure passed to <i>ConfigInfo</i>.

### -param ConfigInfo [in]

Pointer to a <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_server_config_info_vq">DHCP_SERVER_CONFIG_INFO_VQ</a> structure that contains the new or updated settings for the DHCP server.

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
</table>

## -remarks

Most settings are effective immediately and do not require a restart.

The following DHCP server settings require a restart of the DHCP service:<ul>
<li>Set_APIProtocolSupport</li>
<li>Set_DatabaseName</li>
<li>Set_DatabasePath</li>
<li>Set_DatabaseLoggingPath</li>
<li>Set_RestoreFlag</li>
</ul>

## -see-also

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_server_config_info_vq">DHCP_SERVER_CONFIG_INFO_VQ</a>