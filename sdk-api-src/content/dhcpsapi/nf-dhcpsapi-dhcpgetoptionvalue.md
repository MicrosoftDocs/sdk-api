---
UID: NF:dhcpsapi.DhcpGetOptionValue
title: DhcpGetOptionValue function (dhcpsapi.h)
description: The DhcpGetOptionValue function retrieves a DHCP option value (the option code and associated data) for a particular scope.
helpviewer_keywords: ["DhcpGetOptionValue","DhcpGetOptionValue function [DHCP]","dhcp.dhcpgetoptionvalue","dhcpsapi/DhcpGetOptionValue"]
old-location: dhcp\dhcpgetoptionvalue.htm
tech.root: DHCP
ms.assetid: 7dca800f-2427-44b1-bc92-f9db54de08a5
ms.date: 12/05/2018
ms.keywords: DhcpGetOptionValue, DhcpGetOptionValue function [DHCP], dhcp.dhcpgetoptionvalue, dhcpsapi/DhcpGetOptionValue
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
 - DhcpGetOptionValue
 - dhcpsapi/DhcpGetOptionValue
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
 - DhcpGetOptionValue
---

# DhcpGetOptionValue function


## -description

The <b>DhcpGetOptionValue</b> function retrieves a DHCP option value (the option code and associated data) for a particular scope.

## -parameters

### -param ServerIpAddress [in]

Unicode string that specifies the IP address or hostname of the DHCP server.

### -param OptionID [in]

<a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-type-definitions">DHCP_OPTION_ID</a> value that specifies the code for the option value to retrieve.

### -param ScopeInfo [in]

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_option_scope_info">DHCP_OPTION_SCOPE_INFO</a> structure that contains information on the scope where the option value is set.

### -param OptionValue [out]

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_option_value">DHCP_OPTION_VALUE</a> structure that contains the returned option code and data.

<div class="alert"><b>Note</b>  <p class="note">The memory for this parameter must be free using <a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcprpcfreememory">DhcpRpcFreeMemory</a>.

</div>
<div> </div>

## -returns

This function returns <b>ERROR_SUCCESS</b> upon a successful call. Otherwise, it returns one of the <a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-api-error-codes">DHCP Server Management API Error Codes</a>.

## -remarks

This function requires host byte ordering for all <a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-type-definitions">DHCP_IP_ADDRESS</a> values in parameter structures.

## -see-also

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_option_value">DHCP_OPTION_VALUE</a>