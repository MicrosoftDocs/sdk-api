---
UID: NF:dhcpsapi.DhcpGetSubnetInfoV6
title: DhcpGetSubnetInfoV6 function (dhcpsapi.h)
description: The DhcpGetSubnetInfoV6 function returns information on a specific subnet.
helpviewer_keywords: ["DhcpGetSubnetInfoV6","DhcpGetSubnetInfoV6 function [DHCP]","dhcp.dhcpgetsubnetinfov6","dhcpsapi/DhcpGetSubnetInfoV6"]
old-location: dhcp\dhcpgetsubnetinfov6.htm
tech.root: DHCP
ms.assetid: 181015de-c109-4365-a87c-04706f568297
ms.date: 12/05/2018
ms.keywords: DhcpGetSubnetInfoV6, DhcpGetSubnetInfoV6 function [DHCP], dhcp.dhcpgetsubnetinfov6, dhcpsapi/DhcpGetSubnetInfoV6
req.header: dhcpsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - DhcpGetSubnetInfoV6
 - dhcpsapi/DhcpGetSubnetInfoV6
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
 - DhcpGetSubnetInfoV6
---

# DhcpGetSubnetInfoV6 function


## -description

The <b>DhcpGetSubnetInfoV6</b> function returns information on a specific subnet.

## -parameters

### -param ServerIpAddress [in]

Pointer to a Unicode string that specifies the IP address or hostname of the DHCP server.

### -param SubnetAddress [in]

DHCP_IPV6_ADDRESS value that specifies the subnet ID.

### -param SubnetInfo [out]

DHCP_SUBNET_INFO_V6 structure that contains the returned information for the subnet matching the ID specified by <i>SubnetAddress</i>.

<div class="alert"><b>Note</b>  <p class="note">The memory for this parameter must be free using <a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcprpcfreememory">DhcpRpcFreeMemory</a>.

</div>
<div> </div>

## -returns

This function returns <b>ERROR_SUCCESS</b> upon a successful call. Otherwise, it returns one of the <a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-api-error-codes">DHCP Server Management API Error Codes</a>.