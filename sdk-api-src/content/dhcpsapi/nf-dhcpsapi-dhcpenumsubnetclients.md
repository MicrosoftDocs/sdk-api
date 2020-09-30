---
UID: NF:dhcpsapi.DhcpEnumSubnetClients
title: DhcpEnumSubnetClients function (dhcpsapi.h)
description: The DhcpEnumSubnetClients function returns an enumerated list of clients with served IP addresses in the specified subnet.
helpviewer_keywords: ["DhcpEnumSubnetClients","DhcpEnumSubnetClients function [DHCP]","dhcp.dhcpenumsubnetclients","dhcpsapi/DhcpEnumSubnetClients"]
old-location: dhcp\dhcpenumsubnetclients.htm
tech.root: DHCP
ms.assetid: 04ef441e-0638-4ee7-a6a6-a35ab5cf7a44
ms.date: 12/05/2018
ms.keywords: DhcpEnumSubnetClients, DhcpEnumSubnetClients function [DHCP], dhcp.dhcpenumsubnetclients, dhcpsapi/DhcpEnumSubnetClients
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
 - DhcpEnumSubnetClients
 - dhcpsapi/DhcpEnumSubnetClients
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
 - DhcpEnumSubnetClients
---

# DhcpEnumSubnetClients function


## -description

The <b>DhcpEnumSubnetClients</b> function returns an enumerated list of clients with served IP addresses in the specified subnet.

## -parameters

### -param ServerIpAddress [in]

Unicode string that specifies the IP address or hostname of the DHCP server.

### -param SubnetAddress [in]

<a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-type-definitions">DHCP_IP_ADDRESS</a> value that contains the subnet ID. See <a href="https://www.ietf.org/rfc/rfc0950.txt">RFC 950</a> for more information about subnet ID.

### -param ResumeHandle [in, out]

Pointer to a <a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-type-definitions">DHCP_RESUME_HANDLE</a> value that identifies the enumeration operation. Initially, this value should be zero, with a successful call returning the handle value used for subsequent enumeration requests. For example, if <i>PreferredMaximum</i> is set to 1000 bytes, and 2000 bytes worth of subnet client information structures  are stored on the server, the resume handle can be used after the first 1000 bytes are retrieved to obtain the next 1000 on a subsequent call, and so forth.

### -param PreferredMaximum [in]

Specifies the preferred maximum number of bytes of subnet client information structures to return. If the number of remaining unenumerated options (in bytes) is less than this value, then that amount will be returned.   

The minimum value is 1024 bytes (1KB), and the maximum value is 65536 bytes (64KB); if the input value is greater or less than this range, it will be set to the maximum or minimum value, respectively.

### -param ClientInfo [out]

Pointer to a <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_client_info_array">DHCP_CLIENT_INFO_ARRAY</a> structure that contains information on the clients served under this specific subnet. If no clients are available, this field will be null.

### -param ClientsRead [out]

Pointer to a <b>DWORD</b> value that specifies the number of clients returned in <i>ClientInfo</i>.

### -param ClientsTotal [out]

Pointer to a <b>DWORD</b> value that specifies the  number of clients for the specified subnet that have not yet been enumerated.

<div class="alert"><b>Note</b>  This value is set to the correct value during the final enumeration call; however, prior calls to this function set the value as "0x7FFFFFFF".</div>
<div> </div>

## -returns

This function returns <b>ERROR_MORE_DATA</b> upon a successful call. The final call to this method with the last set of subnet clients returns <b>ERROR_SUCCESS</b>. Otherwise, it returns one of the <a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-api-error-codes">DHCP Server Management API Error Codes</a>.

## -remarks

This function requires host byte ordering for all <a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-type-definitions">DHCP_IP_ADDRESS</a> values in parameter structures.

## -see-also

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_client_info_array">DHCP_CLIENT_INFO_ARRAY</a>