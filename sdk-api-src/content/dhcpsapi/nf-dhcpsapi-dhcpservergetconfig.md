---
UID: NF:dhcpsapi.DhcpServerGetConfig
title: DhcpServerGetConfig function (dhcpsapi.h)
description: Returns the specific configuration settings of a DHCP server. (DhcpServerGetConfig)
helpviewer_keywords: ["DhcpServerGetConfig","DhcpServerGetConfig function [DHCP]","dhcp.dhcpservergetconfig","dhcpsapi/DhcpServerGetConfig"]
old-location: dhcp\dhcpservergetconfig.htm
tech.root: DHCP
ms.assetid: 79fa7f78-35ae-4f40-bf3d-3c8f6f323776
ms.date: 12/05/2018
ms.keywords: DhcpServerGetConfig, DhcpServerGetConfig function [DHCP], dhcp.dhcpservergetconfig, dhcpsapi/DhcpServerGetConfig
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
 - DhcpServerGetConfig
 - dhcpsapi/DhcpServerGetConfig
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
 - DhcpServerGetConfig
---

# DhcpServerGetConfig function


## -description

The <b>DhcpServerGetConfig</b> function returns the specific configuration settings of a DHCP server. Configuration information includes information on the JET database used to store subnet and client lease information, and the supported protocols.

## -parameters

### -param ServerIpAddress [in]

Unicode string that specifies the IP address or hostname of the DHCP server.

### -param ConfigInfo [out]

Pointer to a <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_server_config_info">DHCP_SERVER_CONFIG_INFO</a> structure that contains the specific configuration information for the DHCP server.

<div class="alert"><b>Note</b>  <p class="note">The memory for this parameter must be free using <a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcprpcfreememory">DhcpRpcFreeMemory</a>.

</div>
<div> </div>

## -returns

This function returns <b>ERROR_SUCCESS</b> upon a successful call. Otherwise, it returns one of the <a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-api-error-codes">DHCP Server Management API Error Codes</a>.

## -see-also

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_server_config_info">DHCP_SERVER_CONFIG_INFO</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpservergetconfigv4">DhcpServerGetConfigV4</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpserversetconfig">DhcpServerSetConfig</a>
