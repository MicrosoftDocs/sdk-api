---
UID: NF:dhcpsapi.DhcpEnumSubnets
title: DhcpEnumSubnets function (dhcpsapi.h)
description: The DhcpEnumSubnets function returns an enumerated list of subnets defined on the DHCP server.
helpviewer_keywords: ["DhcpEnumSubnets","DhcpEnumSubnets function [DHCP]","dhcp.dhcpenumsubnets","dhcpsapi/DhcpEnumSubnets"]
old-location: dhcp\dhcpenumsubnets.htm
tech.root: DHCP
ms.assetid: 333381c9-66d1-44ef-911b-d543c79abefb
ms.date: 12/05/2018
ms.keywords: DhcpEnumSubnets, DhcpEnumSubnets function [DHCP], dhcp.dhcpenumsubnets, dhcpsapi/DhcpEnumSubnets
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
 - DhcpEnumSubnets
 - dhcpsapi/DhcpEnumSubnets
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
 - DhcpEnumSubnets
---

# DhcpEnumSubnets function


## -description

The <b>DhcpEnumSubnets</b> function returns an enumerated list of subnets defined on the DHCP server.

## -parameters

### -param ServerIpAddress [in]

Unicode string that specifies the IP address or hostname of the DHCP server.

### -param ResumeHandle [in, out]

Pointer to a <a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-type-definitions">DHCP_RESUME_HANDLE</a> value that identifies the enumeration operation. Initially, this value should be zero, with a successful call returning the handle value used for subsequent enumeration requests. For example, if <i>PreferredMaximum</i> is set to 100, and 200 subnet addresses  are stored on the server, the resume handle can be used after the first 100 subnets are retrieved to obtain the next 100 on a subsequent call, and so forth.

### -param PreferredMaximum [in]

Specifies the preferred maximum number of subnet addresses to return. If the number of remaining unenumerated options is less than this value, then that amount will be returned.

### -param EnumInfo [out]

Pointer to a <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_ip_array">DHCP_IP_ARRAY</a> structure that contains the subnet IDs available on the DHCP server. If no subnets are defined, this value will be null.

### -param ElementsRead [out]

Pointer to a <b>DWORD</b> value that specifies the number of subnet addresses returned in <i>EnumInfo</i>.

### -param ElementsTotal [out]

Pointer to a <b>DWORD</b> value that specifies the  number of subnets defined on the DHCP server that have not yet been enumerated.

## -returns

This function returns <b>ERROR_SUCCESS</b> upon a successful call. If a call is made with the same <i>ResumeHandle</i> value and all items on the server have been enumerated, this method returns <b>ERROR_NO_MORE_ITEMS</b> with <i>ElementsRead</i> and <i>ElementsTotal</i> set to 0. Otherwise, it returns one of the <a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-api-error-codes">DHCP Server Management API Error Codes</a>.

## -remarks

When no longer needed, the resources consumed for the  enumerated data, and all pointers contained within, should be released with <a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcprpcfreememory">DhcpRpcFreeMemory</a>.

This function requires host byte ordering for all <a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-type-definitions">DHCP_IP_ADDRESS</a> values in parameter structures.

## -see-also

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_ip_array"> DHCP_IP_ARRAY</a>
