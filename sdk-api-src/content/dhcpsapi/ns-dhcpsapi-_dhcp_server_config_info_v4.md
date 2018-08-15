---
UID: NS:dhcpsapi._DHCP_SERVER_CONFIG_INFO_V4
title: "_DHCP_SERVER_CONFIG_INFO_V4"
author: windows-sdk-content
description: Defines the data used to configure the DHCP server.
old-location: dhcp\dhcp_server_config_info_v4.htm
old-project: dhcp
ms.assetid: a2a78c19-3161-431a-b1af-31dac994c3f6
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*LPDHCP_SERVER_CONFIG_INFO_V4, DHCP_SERVER_CONFIG_INFO_V4, DHCP_SERVER_CONFIG_INFO_V4 structure [DHCP], DHCP_SERVER_USE_RPC_OVER_LPC, DHCP_SERVER_USE_RPC_OVER_NP, DHCP_SERVER_USE_RPC_OVER_TCPIP, LPDHCP_SERVER_CONFIG_INFO_V4, LPDHCP_SERVER_CONFIG_INFO_V4 structure pointer [DHCP], _DHCP_SERVER_CONFIG_INFO_V4, dhcp.dhcp_server_config_info_v4, dhcpsapi/LPDHCP_SERVER_CONFIG_INFO_V4, dhcpsapi/_DHCP_SERVER_CONFIG_INFO_V4"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: dhcpsapi.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: DHCP_SERVER_CONFIG_INFO_V4, *LPDHCP_SERVER_CONFIG_INFO_V4
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Dhcpsapi.h
api_name:
 - DHCP_SERVER_CONFIG_INFO_V4
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _DHCP_SERVER_CONFIG_INFO_V4 structure


## -description


The <b>DHCP_SERVER_CONFIG_INFO_V4</b> structure defines the data used to configure the DHCP server. 


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


### -field dwPingRetries

Specifies a value equal to or greater than 0 or less than 6 that indicates the number of times to ping an unresponsive client before determining unavailability.


### -field cbBootTableString

Specifies the size of <b>wszBootTableString</b>, in bytes.


### -field wszBootTableString

Unicode string that contains the boot table string for the DHCP server. ?? More information needed. ??


### -field wszBootTableString.size_is

 


### -field wszBootTableString.size_is.cbBootTableString/2

 


### -field fAuditLog

Specifies whether or not to enable audit logging on the DHCP server. A value of <b>TRUE</b> indicates that an audit log is generated; <b>FALSE</b> indicates that audit logging is not performed.


## -see-also




<a href="https://msdn.microsoft.com/edbed013-6e17-42f4-b109-9676da80de20">DhcpServerGetConfigV4</a>



<a href="https://msdn.microsoft.com/b2d74c43-5c17-4988-be70-fa152e7f848a">DhcpServerSetConfigV4</a>
 

 

