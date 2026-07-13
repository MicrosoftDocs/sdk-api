---
UID: NF:dhcpsapi.DhcpServerGetConfigV4
title: DhcpServerGetConfigV4 function (dhcpsapi.h)
description: Returns the specific configuration settings of a DHCP server. (DhcpServerGetConfigV4)
helpviewer_keywords: ["DhcpServerGetConfigV4","DhcpServerGetConfigV4 function [DHCP]","dhcp.dhcpservergetconfigv4","dhcpsapi/DhcpServerGetConfigV4"]
old-location: dhcp\dhcpservergetconfigv4.htm
tech.root: DHCP
ms.assetid: edbed013-6e17-42f4-b109-9676da80de20
ms.date: 12/05/2018
ms.keywords: DhcpServerGetConfigV4, DhcpServerGetConfigV4 function [DHCP], dhcp.dhcpservergetconfigv4, dhcpsapi/DhcpServerGetConfigV4
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
 - DhcpServerGetConfigV4
 - dhcpsapi/DhcpServerGetConfigV4
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
 - DhcpServerGetConfigV4
---

# DhcpServerGetConfigV4 function


## -description

The <b>DhcpServerGetConfigV4</b> function returns the specific configuration settings of a DHCP server. This function extends the functionality of DhcpServerGetConfig by adding configuration parameters for the number of ping retries a server uses to determine connectability, the settings for the boot file table, and the audit log state. Configuration information includes information on the JET database used to store subnet and client lease information, and the supported protocols.

## -parameters

### -param ServerIpAddress [in]

Unicode string that specifies the IP address or hostname of the DHCP server.

### -param ConfigInfo [out]

Pointer to a <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_server_config_info_v4">DHCP_SERVER_CONFIG_INFO_V4</a> structure that contains the specific configuration information for the DHCP server.

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



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpserversetconfigv4">DhcpServerSetConfigV4</a>
