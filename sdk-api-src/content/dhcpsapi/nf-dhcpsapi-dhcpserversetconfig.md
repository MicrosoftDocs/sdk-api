---
UID: NF:dhcpsapi.DhcpServerSetConfig
title: DhcpServerSetConfig function
author: windows-sdk-content
description: Configures a DHCPv4 server with specific settings, including information on the JET database used to store subnet and client lease information, and the supported protocols.
old-location: dhcp\dhcpserversetconfig.htm
old-project: DHCP
ms.assetid: 06f0c6b2-a916-4b1b-9956-22dcaafcad1b
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: DhcpServerSetConfig, DhcpServerSetConfig function [DHCP], Set_APIProtocolSupport, Set_BackupInterval, Set_BackupPath, Set_DatabaseCleanupInterval, Set_DatabaseLoggingFlag, Set_DatabaseName, Set_DatabasePath, Set_RestoreFlag, Set_Set_DebugFlag, dhcp.dhcpserversetconfig, dhcpsapi/DhcpServerSetConfig
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: QuarantineStatus
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Dhcpsapi.dll
api_name:
 - DhcpServerSetConfig
product: Windows
targetos: Windows
req.lib: Dhcpsapi.lib
req.dll: Dhcpsapi.dll
req.irql: 
---

# DhcpServerSetConfig function


## -description


The <b>DhcpServerSetConfig</b> function configures a DHCPv4 server with specific settings, including information on the JET database used to store subnet and client lease information, and the supported protocols.


## -parameters




### -param ServerIpAddress [in]

Unicode string that specifies the IP address or hostname of the DHCP server.


### -param FieldsToSet [in]

Specifies a set of bit flags that indicate which fields in <i>ConfigInfo</i> are set. If a flag is present, the corresponding field must also be populated in the <a href="https://msdn.microsoft.com/3c7226fd-703c-4981-b82b-180b4070d671">DHCP_SERVER_CONFIG_INFO</a> structure referenced by <i>ConfigInfo</i>, and will be used to set the same value on the DHCP server,

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
<td width="40%"><a id="Set_Set_DebugFlag"></a><a id="set_set_debugflag"></a><a id="SET_SET_DEBUGFLAG"></a><dl>
<dt><b>Set_Set_DebugFlag</b></dt>
<dt>0x00000100</dt>
</dl>
</td>
<td width="60%">
The <b>DebugFlag</b> field is populated.

</td>
</tr>
</table>
 


### -param ConfigInfo [in]


<a href="https://msdn.microsoft.com/3c7226fd-703c-4981-b82b-180b4070d671">DHCP_SERVER_CONFIG_INFO</a> structure that contains the specific configuration information to set on the DHCP server, as indicated by the flags specified in <i>FieldsToSet</i>.


## -returns



This function returns <b>ERROR_SUCCESS</b> upon a successful call. Otherwise, it returns one of the <a href="https://msdn.microsoft.com/6370313f-d7db-4ff1-b0e0-7fa47474facb">DHCP Server Management API Error Codes</a>.




## -remarks



The DHCPv4 server must be restarted for the following settings to be effective:<ul>
<li>Set_APIProtocolSupport</li>
<li>Set_DatabaseName</li>
<li>Set_DatabasePath</li>
<li>Set_DatabaseLoggingFlag</li>
<li>Set_RestoreFlag</li>
</ul>





## -see-also




<a href="https://msdn.microsoft.com/3c7226fd-703c-4981-b82b-180b4070d671">
        DHCP_SERVER_CONFIG_INFO</a>



<a href="https://msdn.microsoft.com/79fa7f78-35ae-4f40-bf3d-3c8f6f323776">DhcpServerGetConfig</a>



<a href="https://msdn.microsoft.com/b2d74c43-5c17-4988-be70-fa152e7f848a">DhcpServerSetConfigV4</a>
 

 

