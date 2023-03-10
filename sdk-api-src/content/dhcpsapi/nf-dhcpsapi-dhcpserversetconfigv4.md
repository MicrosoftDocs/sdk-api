---
UID: NF:dhcpsapi.DhcpServerSetConfigV4
title: DhcpServerSetConfigV4 function (dhcpsapi.h)
description: The DhcpServerSetConfigV4 function configures a DHCP server with specific settings, including information on the JET database used to store subnet and client lease information, and the supported protocols.
helpviewer_keywords: ["DhcpServerSetConfigV4","DhcpServerSetConfigV4 function [DHCP]","Set_APIProtocolSupport","Set_AuditLogState","Set_BackupInterval","Set_BackupPath","Set_BootFileTable","Set_DatabaseCleanupInterval","Set_DatabaseLoggingFlag","Set_DatabaseName","Set_DatabasePath","Set_DebugFlag","Set_PingRetries","Set_RestoreFlag","dhcp.dhcpserversetconfigv4","dhcpsapi/DhcpServerSetConfigV4"]
old-location: dhcp\dhcpserversetconfigv4.htm
tech.root: DHCP
ms.assetid: b2d74c43-5c17-4988-be70-fa152e7f848a
ms.date: 12/05/2018
ms.keywords: DhcpServerSetConfigV4, DhcpServerSetConfigV4 function [DHCP], Set_APIProtocolSupport, Set_AuditLogState, Set_BackupInterval, Set_BackupPath, Set_BootFileTable, Set_DatabaseCleanupInterval, Set_DatabaseLoggingFlag, Set_DatabaseName, Set_DatabasePath, Set_DebugFlag, Set_PingRetries, Set_RestoreFlag, dhcp.dhcpserversetconfigv4, dhcpsapi/DhcpServerSetConfigV4
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
 - DhcpServerSetConfigV4
 - dhcpsapi/DhcpServerSetConfigV4
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
 - DhcpServerSetConfigV4
---

# DhcpServerSetConfigV4 function


## -description

The <b>DhcpServerSetConfigV4</b> function configures a DHCP server with specific settings, including information on the JET database used to store subnet and client lease information, and the supported protocols.

## -parameters

### -param ServerIpAddress [in]

Unicode string that specifies the IP address or hostname of the DHCP server.

### -param FieldsToSet [in]

Specifies a set of bit flags that indicate which fields in <i>ConfigInfo</i> are set. If a flag is present, the corresponding field must also be populated in the <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_server_config_info_v4">DHCP_SERVER_CONFIG_INFO_V4</a> structure referenced by <i>ConfigInfo</i>, and will be used to set the same value on the DHCP server,

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="Set_APIProtocolSupport"></a><a id="set_apiprotocolsupport"></a><a id="SET_APIPROTOCOLSUPPORT"></a><dl>
<dt><b>Set_APIProtocolSupport</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
The <b>APIProtocolSupport</b> field is populated.

</td>
</tr>
<tr>
<td width="40%"><a id="Set_DatabaseName"></a><a id="set_databasename"></a><a id="SET_DATABASENAME"></a><dl>
<dt><b>Set_DatabaseName</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
The <b>DatabaseName</b> field is populated.

</td>
</tr>
<tr>
<td width="40%"><a id="Set_DatabasePath"></a><a id="set_databasepath"></a><a id="SET_DATABASEPATH"></a><dl>
<dt><b>Set_DatabasePath</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
The <b>DatabasePath</b> field is populated.

</td>
</tr>
<tr>
<td width="40%"><a id="Set_BackupPath"></a><a id="set_backuppath"></a><a id="SET_BACKUPPATH"></a><dl>
<dt><b>Set_BackupPath</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
The <b>BackupPath</b> field is populated.

</td>
</tr>
<tr>
<td width="40%"><a id="Set_BackupInterval"></a><a id="set_backupinterval"></a><a id="SET_BACKUPINTERVAL"></a><dl>
<dt><b>Set_BackupInterval</b></dt>
<dt>0x00000010</dt>
</dl>
</td>
<td width="60%">
The <b>BackupInterval</b> field is populated.

</td>
</tr>
<tr>
<td width="40%"><a id="Set_DatabaseLoggingFlag"></a><a id="set_databaseloggingflag"></a><a id="SET_DATABASELOGGINGFLAG"></a><dl>
<dt><b>Set_DatabaseLoggingFlag</b></dt>
<dt>0x00000020</dt>
</dl>
</td>
<td width="60%">
The <b>DatabaseLoggingFlag</b> field is populated.

</td>
</tr>
<tr>
<td width="40%"><a id="Set_RestoreFlag"></a><a id="set_restoreflag"></a><a id="SET_RESTOREFLAG"></a><dl>
<dt><b>Set_RestoreFlag</b></dt>
<dt>0x00000040</dt>
</dl>
</td>
<td width="60%">
The <b>RestoreFlag</b> field is populated.

</td>
</tr>
<tr>
<td width="40%"><a id="Set_DatabaseCleanupInterval"></a><a id="set_databasecleanupinterval"></a><a id="SET_DATABASECLEANUPINTERVAL"></a><dl>
<dt><b>Set_DatabaseCleanupInterval</b></dt>
<dt>0x00000080</dt>
</dl>
</td>
<td width="60%">
The <b>DatabaseCleanupInterval</b> field is populated.

</td>
</tr>
<tr>
<td width="40%"><a id="Set_DebugFlag"></a><a id="set_debugflag"></a><a id="SET_DEBUGFLAG"></a><dl>
<dt><b>Set_DebugFlag</b></dt>
<dt>0x00000100</dt>
</dl>
</td>
<td width="60%">
The <b>DebugFlag</b> field is populated.

</td>
</tr>
<tr>
<td width="40%"><a id="Set_PingRetries"></a><a id="set_pingretries"></a><a id="SET_PINGRETRIES"></a><dl>
<dt><b>Set_PingRetries</b></dt>
<dt>0x00000200</dt>
</dl>
</td>
<td width="60%">
The <b>PingRetries</b> field is populated.

</td>
</tr>
<tr>
<td width="40%"><a id="Set_BootFileTable"></a><a id="set_bootfiletable"></a><a id="SET_BOOTFILETABLE"></a><dl>
<dt><b>Set_BootFileTable</b></dt>
<dt>0x00000400</dt>
</dl>
</td>
<td width="60%">
The <b>BootFileTable</b> field is populated.

</td>
</tr>
<tr>
<td width="40%"><a id="Set_AuditLogState"></a><a id="set_auditlogstate"></a><a id="SET_AUDITLOGSTATE"></a><dl>
<dt><b>Set_AuditLogState</b></dt>
<dt>0x00000800</dt>
</dl>
</td>
<td width="60%">
The <b>AuditLogState</b> field is populated.

</td>
</tr>
</table>

### -param ConfigInfo [in]

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_server_config_info_v4">DHCP_SERVER_CONFIG_INFO_V4</a> structure that contains the specific DHCP server configuration settings as indicated by the bit flags set in <i>FieldsToSet</i>.

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

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_server_config_info_v4">DHCP_SERVER_CONFIG_INFO_V4</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpservergetconfigv4">DhcpServerGetConfigV4</a>