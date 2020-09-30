---
UID: NF:dhcpsapi.DhcpServerGetConfigVQ
title: DhcpServerGetConfigVQ function (dhcpsapi.h)
description: Retrieves the current DHCP server configuration settings.
helpviewer_keywords: ["DhcpServerGetConfigVQ","DhcpServerGetConfigVQ function [DHCP]","dhcp.dhcpservergetconfigvq","dhcpsapi/DhcpServerGetConfigVQ"]
old-location: dhcp\dhcpservergetconfigvq.htm
tech.root: DHCP
ms.assetid: 77726631-2be0-4ec0-a50f-786e4f3b460a
ms.date: 12/05/2018
ms.keywords: DhcpServerGetConfigVQ, DhcpServerGetConfigVQ function [DHCP], dhcp.dhcpservergetconfigvq, dhcpsapi/DhcpServerGetConfigVQ
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
 - DhcpServerGetConfigVQ
 - dhcpsapi/DhcpServerGetConfigVQ
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
 - DhcpServerGetConfigVQ
---

# DhcpServerGetConfigVQ function


## -description

The <b>DhcpServerGetConfigVQ</b> function retrieves the current DHCP server configuration settings.

## -parameters

### -param ServerIpAddress [in]

Unicode string that specifies the IP address or hostname of the DHCP server.

### -param ConfigInfo [out]

Pointer to the address of a <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_server_config_info_vq">DHCP_SERVER_CONFIG_INFO_VQ</a> structure that contains the returned DHCP server configuration settings.

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

The caller of this function must free the memory pointed to by <i>ConfigInfo</i> by calling <a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcprpcfreememory">DhcpRpcFreeMemory</a>.

## -see-also

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_server_config_info_vq">DHCP_SERVER_CONFIG_INFO_VQ</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpserversetconfigvq">DhcpServerSetConfigVQ</a>