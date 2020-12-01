---
UID: NF:dhcpsapi.DhcpServerSetConfigV6
title: DhcpServerSetConfigV6 function (dhcpsapi.h)
description: Sets the DHCPv6 server configuration data at the scope or server level.
helpviewer_keywords: ["DhcpServerSetConfigV6","DhcpServerSetConfigV6 function [DHCP]","Set_AuditLogState","Set_PreferredLifetime","Set_PreferredLifetimeIATA","Set_RapidCommitFlag","Set_T1","Set_T2","Set_UnicastFlag","Set_ValidLifetime","Set_ValidLifetimeIATA","dhcp.dhcpserversetconfigv6","dhcpsapi/DhcpServerSetConfigV6"]
old-location: dhcp\dhcpserversetconfigv6.htm
tech.root: DHCP
ms.assetid: 6e24b1d8-ae76-4834-9c44-f1dcae946fa9
ms.date: 12/05/2018
ms.keywords: DhcpServerSetConfigV6, DhcpServerSetConfigV6 function [DHCP], Set_AuditLogState, Set_PreferredLifetime, Set_PreferredLifetimeIATA, Set_RapidCommitFlag, Set_T1, Set_T2, Set_UnicastFlag, Set_ValidLifetime, Set_ValidLifetimeIATA, dhcp.dhcpserversetconfigv6, dhcpsapi/DhcpServerSetConfigV6
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
 - DhcpServerSetConfigV6
 - dhcpsapi/DhcpServerSetConfigV6
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
 - DhcpServerSetConfigV6
---

# DhcpServerSetConfigV6 function


## -description

The <b>DhcpServerSetConfigV6</b> function sets the DHCPv6 server configuration data at the scope or server level.

## -parameters

### -param ServerIpAddress [in]

Unicode string that specifies the IP address or hostname of the DHCP server.

### -param ScopeInfo [in]

Pointer to a <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_option_scope_info6">DHCP_OPTION_SCOPE_INFO6</a> structure that contains the configuration information at the scope or server level.

### -param FieldsToSet [in]

Specifies the set of value that indicate the type of configuration information provided in <i>ConfigInfo</i>. Only one of these values may be set per call.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="Set_UnicastFlag"></a><a id="set_unicastflag"></a><a id="SET_UNICASTFLAG"></a><dl>
<dt><b>Set_UnicastFlag</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Not used.

</td>
</tr>
<tr>
<td width="40%"><a id="Set_RapidCommitFlag"></a><a id="set_rapidcommitflag"></a><a id="SET_RAPIDCOMMITFLAG"></a><dl>
<dt><b>Set_RapidCommitFlag</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
Not used.

</td>
</tr>
<tr>
<td width="40%"><a id="Set_PreferredLifetime"></a><a id="set_preferredlifetime"></a><a id="SET_PREFERREDLIFETIME"></a><dl>
<dt><b>Set_PreferredLifetime</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
Sets the preferred lifetime value for a non-temporary IPv6 address.

</td>
</tr>
<tr>
<td width="40%"><a id="Set_ValidLifetime"></a><a id="set_validlifetime"></a><a id="SET_VALIDLIFETIME"></a><dl>
<dt><b>Set_ValidLifetime</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
Sets the valid lifetime value for a non-temporary IPv6 address.

</td>
</tr>
<tr>
<td width="40%"><a id="Set_T1"></a><a id="set_t1"></a><a id="SET_T1"></a><dl>
<dt><b>Set_T1</b></dt>
<dt>0x00000010</dt>
</dl>
</td>
<td width="60%">
Sets the T1 time value.

</td>
</tr>
<tr>
<td width="40%"><a id="Set_T2"></a><a id="set_t2"></a><a id="SET_T2"></a><dl>
<dt><b>Set_T2</b></dt>
<dt>0x00000020</dt>
</dl>
</td>
<td width="60%">
Sets the T2 time value.

</td>
</tr>
<tr>
<td width="40%"><a id="Set_PreferredLifetimeIATA"></a><a id="set_preferredlifetimeiata"></a><a id="SET_PREFERREDLIFETIMEIATA"></a><dl>
<dt><b>Set_PreferredLifetimeIATA</b></dt>
<dt>0x00000040</dt>
</dl>
</td>
<td width="60%">
Not used.

</td>
</tr>
<tr>
<td width="40%"><a id="Set_ValidLifetimeIATA"></a><a id="set_validlifetimeiata"></a><a id="SET_VALIDLIFETIMEIATA"></a><dl>
<dt><b>Set_ValidLifetimeIATA</b></dt>
<dt>0x00000080</dt>
</dl>
</td>
<td width="60%">
Not used.

</td>
</tr>
<tr>
<td width="40%"><a id="Set_AuditLogState"></a><a id="set_auditlogstate"></a><a id="SET_AUDITLOGSTATE"></a><dl>
<dt><b>Set_AuditLogState</b></dt>
<dt>0x00000800</dt>
</dl>
</td>
<td width="60%">
Sets the audit log state in the registry.

</td>
</tr>
</table>

### -param ConfigInfo [in]

Pointer to a <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_server_config_info_v6">DHCP_SERVER_CONFIG_INFO_V6</a> structure that contains configuration information of the type indicated by the value supplied in <i>FieldsToSet</i>.

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
<dt><b>ERROR_DHCP_JET_ERROR</b></dt>
</dl>
</td>
<td width="60%">
An error occurred while accessing the DHCP server's database.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_server_config_info_v6">DHCP_SERVER_CONFIG_INFO_V6</a>