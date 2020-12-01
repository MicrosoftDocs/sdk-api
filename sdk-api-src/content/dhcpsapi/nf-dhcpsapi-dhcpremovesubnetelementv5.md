---
UID: NF:dhcpsapi.DhcpRemoveSubnetElementV5
title: DhcpRemoveSubnetElementV5 function (dhcpsapi.h)
description: The DhcpRemoveSubnetElementV5 function removes an element from a subnet defined on the DHCP server.
helpviewer_keywords: ["DhcpRemoveSubnetElementV5","DhcpRemoveSubnetElementV5 function [DHCP]","dhcp.dhcpremovesubnetelementv5","dhcpsapi/DhcpRemoveSubnetElementV5"]
old-location: dhcp\dhcpremovesubnetelementv5.htm
tech.root: DHCP
ms.assetid: 8232b2cc-0bb1-4509-ad5f-6d1d1ece9fe5
ms.date: 12/05/2018
ms.keywords: DhcpRemoveSubnetElementV5, DhcpRemoveSubnetElementV5 function [DHCP], dhcp.dhcpremovesubnetelementv5, dhcpsapi/DhcpRemoveSubnetElementV5
req.header: dhcpsapi.h
req.include-header: 
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
req.lib: Dhcpsapi.lib
req.dll: Dhcpsapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DhcpRemoveSubnetElementV5
 - dhcpsapi/DhcpRemoveSubnetElementV5
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
 - DhcpRemoveSubnetElementV5
---

# DhcpRemoveSubnetElementV5 function


## -description

The <b>DhcpRemoveSubnetElementV5</b> function removes an element from a subnet defined on the DHCP server.

## -parameters

### -param ServerIpAddress [in, optional]

Pointer to a Unicode string that specifies the IP address or hostname of the DHCP server.

### -param SubnetAddress [in]

<a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-type-definitions">DHCP_IP_ADDRESS</a> value that specifies the IP address of the subnet gateway and uniquely identifies it.

### -param RemoveElementInfo [in]

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_subnet_element_data_v5">DHCP_SUBNET_ELEMENT_DATA_V5</a> structure that contains information used to find the element that will be removed from subnet specified in <i>SubnetAddress</i>.

### -param ForceFlag [in]

<a href="/windows/desktop/api/dhcpsapi/ne-dhcpsapi-dhcp_force_flag">DHCP_FORCE_FLAG</a> enumeration value that indicates whether or not the clients affected by the removal of the subnet element should also be deleted.

## -returns

This function returns <b>ERROR_SUCCESS</b> upon a successful call. Otherwise, it returns one of the <a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-api-error-codes">DHCP Server Management API Error Codes</a>.

## -remarks

This function emulates the RPC interface used by the Windows NT 4.0 DHCP server. It is provided for backward compatibility with older versions of the DHCP Administrator application.

## -see-also

<a href="/windows/desktop/api/dhcpsapi/ne-dhcpsapi-dhcp_force_flag">DHCP_FORCE_FLAG</a>



<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_subnet_element_data_v5">DHCP_SUBNET_ELEMENT_DATA_V5</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpaddsubnetelementv5">DhcpAddSubnetElementV5</a>