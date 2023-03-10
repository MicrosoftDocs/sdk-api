---
UID: NS:dhcpsapi._DHCP_SERVER_CONFIG_INFO_VQ
title: DHCP_SERVER_CONFIG_INFO_VQ (dhcpsapi.h)
description: Defines settings for the DHCP server.
helpviewer_keywords: ["*LPDHCP_SERVER_CONFIG_INFO_VQ","DEBUG_ADDRESS","DEBUG_ALLOC","DEBUG_APIS","DEBUG_API_VERBOSE","DEBUG_AUDITLOG","DEBUG_CLIENT","DEBUG_DNS","DEBUG_ERRORS","DEBUG_INIT","DEBUG_JET","DEBUG_LOG_IN_FILE","DEBUG_MESSAGE","DEBUG_MISC","DEBUG_MSTOC","DEBUG_OPTIONS","DEBUG_PARAMETERS","DEBUG_PERF","DEBUG_PING","DEBUG_PNP","DEBUG_QUARANTINE","DEBUG_REGISTRY","DEBUG_ROGUE","DEBUG_SCAVENGER","DEBUG_STARTUP_BRK","DEBUG_STOC","DEBUG_THREAD","DEBUG_THREADPOOL","DEBUG_TIMESTAMP","DEBUG_TRACE","DEBUG_TRACE_CALLS","DEBUG_TRACK","DHCP_SERVER_CONFIG_INFO_VQ","DHCP_SERVER_CONFIG_INFO_VQ structure [DHCP]","DHCP_SERVER_USE_RPC_OVER_ALL","DHCP_SERVER_USE_RPC_OVER_LPC","DHCP_SERVER_USE_RPC_OVER_NP","DHCP_SERVER_USE_RPC_OVER_TCPIP","PDHCP_SERVER_CONFIG_INFO_VQ","PDHCP_SERVER_CONFIG_INFO_VQ structure pointer [DHCP]","dhcp.dhcp_server_config_info_vq","dhcpsapi/DHCP_SERVER_CONFIG_INFO_VQ","dhcpsapi/PDHCP_SERVER_CONFIG_INFO_VQ"]
old-location: dhcp\dhcp_server_config_info_vq.htm
tech.root: DHCP
ms.assetid: 54b5898f-8e9d-42be-b68e-32884d3dbe08
ms.date: 12/05/2018
ms.keywords: '*LPDHCP_SERVER_CONFIG_INFO_VQ, DEBUG_ADDRESS, DEBUG_ALLOC, DEBUG_APIS, DEBUG_API_VERBOSE, DEBUG_AUDITLOG, DEBUG_CLIENT, DEBUG_DNS, DEBUG_ERRORS, DEBUG_INIT, DEBUG_JET, DEBUG_LOG_IN_FILE, DEBUG_MESSAGE, DEBUG_MISC, DEBUG_MSTOC, DEBUG_OPTIONS, DEBUG_PARAMETERS, DEBUG_PERF, DEBUG_PING, DEBUG_PNP, DEBUG_QUARANTINE, DEBUG_REGISTRY, DEBUG_ROGUE, DEBUG_SCAVENGER, DEBUG_STARTUP_BRK, DEBUG_STOC, DEBUG_THREAD, DEBUG_THREADPOOL, DEBUG_TIMESTAMP, DEBUG_TRACE, DEBUG_TRACE_CALLS, DEBUG_TRACK, DHCP_SERVER_CONFIG_INFO_VQ, DHCP_SERVER_CONFIG_INFO_VQ structure [DHCP], DHCP_SERVER_USE_RPC_OVER_ALL, DHCP_SERVER_USE_RPC_OVER_LPC, DHCP_SERVER_USE_RPC_OVER_NP, DHCP_SERVER_USE_RPC_OVER_TCPIP, PDHCP_SERVER_CONFIG_INFO_VQ, PDHCP_SERVER_CONFIG_INFO_VQ structure pointer [DHCP], dhcp.dhcp_server_config_info_vq, dhcpsapi/DHCP_SERVER_CONFIG_INFO_VQ, dhcpsapi/PDHCP_SERVER_CONFIG_INFO_VQ'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: DHCP_SERVER_CONFIG_INFO_VQ, *LPDHCP_SERVER_CONFIG_INFO_VQ
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DHCP_SERVER_CONFIG_INFO_VQ
 - dhcpsapi/_DHCP_SERVER_CONFIG_INFO_VQ
 - LPDHCP_SERVER_CONFIG_INFO_VQ
 - dhcpsapi/LPDHCP_SERVER_CONFIG_INFO_VQ
 - DHCP_SERVER_CONFIG_INFO_VQ
 - dhcpsapi/DHCP_SERVER_CONFIG_INFO_VQ
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
 - DHCP_SERVER_CONFIG_INFO_VQ
---

# DHCP_SERVER_CONFIG_INFO_VQ structure


## -description

The <b>DHCP_SERVER_CONFIG_INFO_VQ</b> structure defines settings for the DHCP server.

## -struct-fields

### -field APIProtocolSupport

Integer value that defines the type of RPC protocol used by the DHCP server to register with RPC. Following is the set of supported types, which may be bitwise OR'd to produce valid values.

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
RPC protocol over TCP is used by the DHCP server to register.

</td>
</tr>
<tr>
<td width="40%"><a id="DHCP_SERVER_USE_RPC_OVER_NP"></a><a id="dhcp_server_use_rpc_over_np"></a><dl>
<dt><b>DHCP_SERVER_USE_RPC_OVER_NP</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
RPC protocol over named pipes is used by the DHCP server to register.&lt;8&gt;

</td>
</tr>
<tr>
<td width="40%"><a id="DHCP_SERVER_USE_RPC_OVER_LPC"></a><a id="dhcp_server_use_rpc_over_lpc"></a><dl>
<dt><b>DHCP_SERVER_USE_RPC_OVER_LPC</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
RPC protocol over LPC is used by the DHCP server to register.&lt;9&gt;

</td>
</tr>
<tr>
<td width="40%"><a id="DHCP_SERVER_USE_RPC_OVER_ALL"></a><a id="dhcp_server_use_rpc_over_all"></a><dl>
<dt><b>DHCP_SERVER_USE_RPC_OVER_ALL</b></dt>
<dt>0x00000007</dt>
</dl>
</td>
<td width="60%">
The DHCP server supports all of the preceding protocols.

</td>
</tr>
</table>

### -field DatabaseName

Pointer to a null-terminated Unicode string that represents the DHCP server database name that is used by the DHCP server for persistent storage.

### -field DatabasePath

Pointer to a null-terminated Unicode string that contains the absolute path, where the DHCP server database is stored.

### -field BackupPath

Pointer to a null-terminated Unicode string that contains the absolute path for backup storage that is used by the DHCP server for backup.

### -field BackupInterval

Integer value that specifies the interval in minutes between backups of the DHCP server database.

### -field DatabaseLoggingFlag

Integer value that indicates the transaction logging mode of the DHCP server. The value 1 indicates that the transaction log is enabled for the DHCP server, and 0 indicates that the transaction log is disabled for the DHCP server.

### -field RestoreFlag

Integer value used as a BOOL flag. If this setting is <b>TRUE</b> (1), the DHCP service loads the DHCP database from the backup database on DHCP service startup. The default value of this flag is <b>FALSE</b> (0).

### -field DatabaseCleanupInterval

Integer value that specifies the maximum time interval that DOOMED IPv4 DHCP client records are allowed to persist within the DHCP server database.

### -field DebugFlag

Integer flag value that specifies the level of logging done by the DHCP server. The following table defines the set values that can be used. Specifying '0xFFFFFFFF' enables all types of logging.

LOW WORD bitmask (0x0000FFFF) for low-frequency debug output.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DEBUG_ADDRESS"></a><a id="debug_address"></a><dl>
<dt><b>DEBUG_ADDRESS</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Enable IP-address-related logging.

</td>
</tr>
<tr>
<td width="40%"><a id="DEBUG_CLIENT"></a><a id="debug_client"></a><dl>
<dt><b>DEBUG_CLIENT</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
Enable DHCP-client-API-related logging.

</td>
</tr>
<tr>
<td width="40%"><a id="DEBUG_PARAMETERS"></a><a id="debug_parameters"></a><dl>
<dt><b>DEBUG_PARAMETERS</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
Enable DHCP-server-parameters-related logging.

</td>
</tr>
<tr>
<td width="40%"><a id="DEBUG_OPTIONS"></a><a id="debug_options"></a><dl>
<dt><b>DEBUG_OPTIONS</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
Enable DHCP-options-related logging.

</td>
</tr>
<tr>
<td width="40%"><a id="DEBUG_ERRORS"></a><a id="debug_errors"></a><dl>
<dt><b>DEBUG_ERRORS</b></dt>
<dt>0x00000010</dt>
</dl>
</td>
<td width="60%">
Enable DHCP-errors-related logging.

</td>
</tr>
<tr>
<td width="40%"><a id="DEBUG_STOC"></a><a id="debug_stoc"></a><dl>
<dt><b>DEBUG_STOC</b></dt>
<dt>0x00000020</dt>
</dl>
</td>
<td width="60%">
Enable DHCPv4 and DCHPv6-protocol-errors-related logging.

</td>
</tr>
<tr>
<td width="40%"><a id="DEBUG_INIT"></a><a id="debug_init"></a><dl>
<dt><b>DEBUG_INIT</b></dt>
<dt>0x00000040</dt>
</dl>
</td>
<td width="60%">
Enable DHCP-server-initialization-related logging.

</td>
</tr>
<tr>
<td width="40%"><a id="DEBUG_SCAVENGER"></a><a id="debug_scavenger"></a><dl>
<dt><b>DEBUG_SCAVENGER</b></dt>
<dt>0x00000080</dt>
</dl>
</td>
<td width="60%">
Enable scavenger's-error-related logging.

</td>
</tr>
<tr>
<td width="40%"><a id="DEBUG_TIMESTAMP"></a><a id="debug_timestamp"></a><dl>
<dt><b>DEBUG_TIMESTAMP</b></dt>
<dt>0x00000100</dt>
</dl>
</td>
<td width="60%">
Enable timing-errors-related logging.

</td>
</tr>
<tr>
<td width="40%"><a id="DEBUG_APIS"></a><a id="debug_apis"></a><dl>
<dt><b>DEBUG_APIS</b></dt>
<dt>0x00000200</dt>
</dl>
</td>
<td width="60%">
Enable DHCP-APIs-related logging.

</td>
</tr>
<tr>
<td width="40%"><a id="DEBUG_REGISTRY"></a><a id="debug_registry"></a><dl>
<dt><b>DEBUG_REGISTRY</b></dt>
<dt>0x00000400</dt>
</dl>
</td>
<td width="60%">
Enable the logging of errors caused by registry setting operations.

</td>
</tr>
<tr>
<td width="40%"><a id="DEBUG_JET"></a><a id="debug_jet"></a><dl>
<dt><b>DEBUG_JET</b></dt>
<dt>0x00000800</dt>
</dl>
</td>
<td width="60%">
Enable the logging of the DHCP server database errors.

</td>
</tr>
<tr>
<td width="40%"><a id="DEBUG_THREADPOOL"></a><a id="debug_threadpool"></a><dl>
<dt><b>DEBUG_THREADPOOL</b></dt>
<dt>0x00001000</dt>
</dl>
</td>
<td width="60%">
Enable the logging related to executing thread pool operations.

</td>
</tr>
<tr>
<td width="40%"><a id="DEBUG_AUDITLOG"></a><a id="debug_auditlog"></a><dl>
<dt><b>DEBUG_AUDITLOG</b></dt>
<dt>0x00002000</dt>
</dl>
</td>
<td width="60%">
Enable the logging related to errors caused by audit log operations.

</td>
</tr>
<tr>
<td width="40%"><a id="DEBUG_QUARANTINE"></a><a id="debug_quarantine"></a><dl>
<dt><b>DEBUG_QUARANTINE</b></dt>
<dt>0x00004000</dt>
</dl>
</td>
<td width="60%">
Enable the logging of errors caused by quarantine errors.

</td>
</tr>
<tr>
<td width="40%"><a id="DEBUG_MISC"></a><a id="debug_misc"></a><dl>
<dt><b>DEBUG_MISC</b></dt>
<dt>0x00008000</dt>
</dl>
</td>
<td width="60%">
Enable the logging caused by miscellaneous errors.

</td>
</tr>
</table>
 

HIGH WORD bitmask (0xFFFF0000) for high-frequency debug output, that is, more verbose.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DEBUG_MESSAGE"></a><a id="debug_message"></a><dl>
<dt><b>DEBUG_MESSAGE</b></dt>
<dt>0x00010000</dt>
</dl>
</td>
<td width="60%">
Enable the logging related to debug messages.

</td>
</tr>
<tr>
<td width="40%"><a id="DEBUG_API_VERBOSE"></a><a id="debug_api_verbose"></a><dl>
<dt><b>DEBUG_API_VERBOSE</b></dt>
<dt>0x00020000</dt>
</dl>
</td>
<td width="60%">
Enable the logging related to DHCP API verbose errors.

</td>
</tr>
<tr>
<td width="40%"><a id="DEBUG_DNS"></a><a id="debug_dns"></a><dl>
<dt><b>DEBUG_DNS</b></dt>
<dt>0x00040000</dt>
</dl>
</td>
<td width="60%">
Enable the logging related to DNS messages.

</td>
</tr>
<tr>
<td width="40%"><a id="DEBUG_MSTOC"></a><a id="debug_mstoc"></a><dl>
<dt><b>DEBUG_MSTOC</b></dt>
<dt>0x00080000</dt>
</dl>
</td>
<td width="60%">
Enable the logging related to multicast protocol layer errors.

</td>
</tr>
<tr>
<td width="40%"><a id="DEBUG_TRACK"></a><a id="debug_track"></a><dl>
<dt><b>DEBUG_TRACK</b></dt>
<dt>0x00100000</dt>
</dl>
</td>
<td width="60%">
Enable the logging tracking specific problems.

</td>
</tr>
<tr>
<td width="40%"><a id="DEBUG_ROGUE"></a><a id="debug_rogue"></a><dl>
<dt><b>DEBUG_ROGUE</b></dt>
<dt>0x00200000</dt>
</dl>
</td>
<td width="60%">
Enable the logging related to a ROGUE DHCP server.

</td>
</tr>
<tr>
<td width="40%"><a id="DEBUG_PNP"></a><a id="debug_pnp"></a><dl>
<dt><b>DEBUG_PNP</b></dt>
<dt>0x00400000</dt>
</dl>
</td>
<td width="60%">
Enable the logging related to PNP interface errors.

</td>
</tr>
<tr>
<td width="40%"><a id="DEBUG_PERF"></a><a id="debug_perf"></a><dl>
<dt><b>DEBUG_PERF</b></dt>
<dt>0x01000000</dt>
</dl>
</td>
<td width="60%">
Enable the logging of performance-related messages.

</td>
</tr>
<tr>
<td width="40%"><a id="DEBUG_ALLOC"></a><a id="debug_alloc"></a><dl>
<dt><b>DEBUG_ALLOC</b></dt>
<dt>0x02000000</dt>
</dl>
</td>
<td width="60%">
Enable the logging of allocation-related and deallocation-related messages.

</td>
</tr>
<tr>
<td width="40%"><a id="DEBUG_PING"></a><a id="debug_ping"></a><dl>
<dt><b>DEBUG_PING</b></dt>
<dt>0x04000000</dt>
</dl>
</td>
<td width="60%">
Enable the logging of synchronous ping–related messages.

</td>
</tr>
<tr>
<td width="40%"><a id="DEBUG_THREAD"></a><a id="debug_thread"></a><dl>
<dt><b>DEBUG_THREAD</b></dt>
<dt>0x08000000</dt>
</dl>
</td>
<td width="60%">
Enable the logging of thread-related messages.

</td>
</tr>
<tr>
<td width="40%"><a id="DEBUG_TRACE"></a><a id="debug_trace"></a><dl>
<dt><b>DEBUG_TRACE</b></dt>
<dt>0x10000000</dt>
</dl>
</td>
<td width="60%">
Enable the logging for tracing through code messages.

</td>
</tr>
<tr>
<td width="40%"><a id="DEBUG_TRACE_CALLS"></a><a id="debug_trace_calls"></a><dl>
<dt><b>DEBUG_TRACE_CALLS</b></dt>
<dt>0x20000000</dt>
</dl>
</td>
<td width="60%">
Enable the logging for tracing through piles of code.

</td>
</tr>
<tr>
<td width="40%"><a id="DEBUG_STARTUP_BRK"></a><a id="debug_startup_brk"></a><dl>
<dt><b>DEBUG_STARTUP_BRK</b></dt>
<dt>0x40000000</dt>
</dl>
</td>
<td width="60%">
Enable the logging related to debugger break during setup messages.

</td>
</tr>
<tr>
<td width="40%"><a id="DEBUG_LOG_IN_FILE"></a><a id="debug_log_in_file"></a><dl>
<dt><b>DEBUG_LOG_IN_FILE</b></dt>
<dt>0x80000000</dt>
</dl>
</td>
<td width="60%">
Enable the logging of debug output in a file.

</td>
</tr>
</table>

### -field dwPingRetries

Integer value that specifies the number of retries that the DHCP server can make to verify whether a particular address is already in use by any client by issuing a ping before issuing any address to the DHCP client (valid range: 0–5, inclusive).

### -field cbBootTableString

Integer value that contains the size of the BOOT TABLE given to the DHCP client.

### -field wszBootTableString

Pointer to a null-terminated Unicode string that contains the absolute path of the BOOTP TABLE given to the BOOTP client.

### -field wszBootTableString.size_is

### -field wszBootTableString.size_is.cbBootTableString/2

### -field fAuditLog

If <b>TRUE</b>, an audit log will be written by the DHCP server; if <b>FALSE</b>, it will not.

### -field QuarantineOn

If <b>TRUE</b>, Quarantine is turned ON on the DHCP server; if <b>FALSE</b>, it is turned OFF.

### -field QuarDefFail

Integer value that determines the default policy for a DHCP NAP server when an NPS server is not reachable. Choices include Quarantine/unrestricted/Drop Request.

### -field QuarRuntimeStatus

If <b>TRUE</b>, NAP is enabled on the DHCP server; if <b>FALSE</b>, it is not.

