---
UID: NS:dhcpsapi._DHCP_SERVER_CONFIG_INFO
title: DHCP_SERVER_CONFIG_INFO (dhcpsapi.h)
description: The DHCP_SERVER_CONFIG_INFO structure defines the data used to configure the DHCP server.
helpviewer_keywords: ["*LPDHCP_SERVER_CONFIG_INFO","DHCP_SERVER_CONFIG_INFO","DHCP_SERVER_CONFIG_INFO structure [DHCP]","DHCP_SERVER_USE_RPC_OVER_LPC","DHCP_SERVER_USE_RPC_OVER_NP","DHCP_SERVER_USE_RPC_OVER_TCPIP","LPDHCP_SERVER_CONFIG_INFO","LPDHCP_SERVER_CONFIG_INFO structure pointer [DHCP]","dhcp.dhcp_server_config_info","dhcpsapi/LPDHCP_SERVER_CONFIG_INFO","dhcpsapi/_DHCP_SERVER_CONFIG_INFO"]
old-location: dhcp\dhcp_server_config_info.htm
tech.root: DHCP
ms.assetid: 3c7226fd-703c-4981-b82b-180b4070d671
ms.date: 12/05/2018
ms.keywords: '*LPDHCP_SERVER_CONFIG_INFO, DHCP_SERVER_CONFIG_INFO, DHCP_SERVER_CONFIG_INFO structure [DHCP], DHCP_SERVER_USE_RPC_OVER_LPC, DHCP_SERVER_USE_RPC_OVER_NP, DHCP_SERVER_USE_RPC_OVER_TCPIP, LPDHCP_SERVER_CONFIG_INFO, LPDHCP_SERVER_CONFIG_INFO structure pointer [DHCP], dhcp.dhcp_server_config_info, dhcpsapi/LPDHCP_SERVER_CONFIG_INFO, dhcpsapi/_DHCP_SERVER_CONFIG_INFO'
req.header: dhcpsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: Windows Server 2003
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: DHCP_SERVER_CONFIG_INFO, *LPDHCP_SERVER_CONFIG_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DHCP_SERVER_CONFIG_INFO
 - dhcpsapi/_DHCP_SERVER_CONFIG_INFO
 - LPDHCP_SERVER_CONFIG_INFO
 - dhcpsapi/LPDHCP_SERVER_CONFIG_INFO
 - DHCP_SERVER_CONFIG_INFO
 - dhcpsapi/DHCP_SERVER_CONFIG_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Dhcpsapi.h
api_name:
 - DHCP_SERVER_CONFIG_INFO
---

# DHCP_SERVER_CONFIG_INFO structure


## -description

The <b>DHCP_SERVER_CONFIG_INFO</b> structure defines the data used to configure the DHCP server.

## -struct-fields

### -field APIProtocolSupport

Specifies a set of bit flags that contain the RPC protocols supported by the DHCP server.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DHCP_SERVER_USE_RPC_OVER_TCPIP"></a><a id="dhcp_server_use_rpc_over_tcpip"></a><dl>
<dt><b>DHCP_SERVER_USE_RPC_OVER_TCPIP</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
TCP/IP can be used for DHCP API RPC calls.

</td>
</tr>
<tr>
<td width="40%"><a id="DHCP_SERVER_USE_RPC_OVER_NP"></a><a id="dhcp_server_use_rpc_over_np"></a><dl>
<dt><b>DHCP_SERVER_USE_RPC_OVER_NP</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
Named pipes can be used for DHCP API RPC calls.

</td>
</tr>
<tr>
<td width="40%"><a id="DHCP_SERVER_USE_RPC_OVER_LPC"></a><a id="dhcp_server_use_rpc_over_lpc"></a><dl>
<dt><b>DHCP_SERVER_USE_RPC_OVER_LPC</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
Local Procedure Call (LPC) can be used for local DHCP API RPC calls.

</td>
</tr>
</table>

### -field DatabaseName

Unicode string that specifies the  file name of the client lease JET database.

### -field DatabasePath

Unicode string that specifies the absolute path to <b>DatabaseName</b>.

### -field BackupPath

Unicode string that specifies the absolute path and file name of the backup client lease JET database.

### -field BackupInterval

Specifies the interval, in minutes,  between backups of the client lease database.

### -field DatabaseLoggingFlag

Specifies a bit flag that indicates whether or not database actions should be logged.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
All database operations will be logged.

</td>
</tr>
</table>

### -field RestoreFlag

Specifies a bit flag that indicates whether or not a database restore operation should be performed.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
The client lease database should be restored from the path and file specified in <b>BackupPath</b>.

</td>
</tr>
</table>

### -field DatabaseCleanupInterval

Specifies the interval, in minutes,  between cleanup operations  performed on the client lease database.

### -field DebugFlag

Reserved. This field should be set to 0x00000000.

## -see-also

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_server_config_info_v4">DHCP_SERVER_CONFIG_INFO_V4</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpservergetconfig">DhcpServerGetConfig</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpserversetconfig">DhcpServerSetConfig</a>