---
UID: NF:dhcpsapi.DhcpDeleteSubnet
title: DhcpDeleteSubnet function (dhcpsapi.h)
description: The DhcpDeleteSubnet function deletes a subnet from the DHCP server.
helpviewer_keywords: ["DhcpDeleteSubnet","DhcpDeleteSubnet function [DHCP]","dhcp.dhcpdeletesubnet","dhcpsapi/DhcpDeleteSubnet"]
old-location: dhcp\dhcpdeletesubnet.htm
tech.root: DHCP
ms.assetid: e000a81b-b61b-4ba9-adee-4940edc78050
ms.date: 12/05/2018
ms.keywords: DhcpDeleteSubnet, DhcpDeleteSubnet function [DHCP], dhcp.dhcpdeletesubnet, dhcpsapi/DhcpDeleteSubnet
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
 - DhcpDeleteSubnet
 - dhcpsapi/DhcpDeleteSubnet
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
 - DhcpDeleteSubnet
---

# DhcpDeleteSubnet function


## -description

The <b>DhcpDeleteSubnet</b> function deletes a subnet from the DHCP server.

## -parameters

### -param ServerIpAddress [in]

Unicode string that specifies the IP address of the subnet to delete.

### -param SubnetAddress [in]

<a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-type-definitions">DHCP_IP_ADDRESS</a> value that contains the IP address of the subnet gateway used to identify the subnet.

### -param ForceFlag [in]

<a href="/windows/desktop/api/dhcpsapi/ne-dhcpsapi-dhcp_force_flag">DHCP_FORCE_FLAG</a> enumeration value that indicates the type of delete operation to perform (full force, failover force, or no force).

## -returns

This function returns <b>ERROR_SUCCESS</b> upon a successful call. Otherwise, it returns one of the <a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-api-error-codes">DHCP Server Management API Error Codes</a>.

## -remarks

Usually, you will use either <b>DhcpFullForce</b> or <b>DhcpNoForce</b> as the value for <i>ForceFlag</i>. The <b>DhcpFailoverForce</b> value is intended for use when cleaning up a broken or improperly configured DHCP failover configuration. In that case, use of <b>DhcpFailoverForce</b> ensures that the entire DNS configuration isn't improperly deleted while cleaning up the DHCP failover configuration. Note that the minimum server OS requirement for <b>DhcpFailoverForce</b> is Windows Server 2012 R2 with KB 3100473 installed.

## -see-also

<a href="/windows/desktop/api/dhcpsapi/ne-dhcpsapi-dhcp_force_flag"> DHCP_FORCE_FLAG</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpcreatesubnet">DhcpCreateSubnet</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpenumsubnets">DhcpEnumSubnets</a>