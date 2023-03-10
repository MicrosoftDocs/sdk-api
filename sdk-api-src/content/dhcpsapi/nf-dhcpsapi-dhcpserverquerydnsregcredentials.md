---
UID: NF:dhcpsapi.DhcpServerQueryDnsRegCredentials
title: DhcpServerQueryDnsRegCredentials function (dhcpsapi.h)
description: Retrieves the current Domain Name System (DNS) credentials used by the DHCP server for client dynamic DNS registration.
helpviewer_keywords: ["DhcpServerQueryDnsRegCredentials","DhcpServerQueryDnsRegCredentials function [DHCP]","dhcp.dhcpserverquerydnsregcredentials","dhcpsapi/DhcpServerQueryDnsRegCredentials"]
old-location: dhcp\dhcpserverquerydnsregcredentials.htm
tech.root: DHCP
ms.assetid: 773cbfef-1dc5-4d44-9997-591acbfb3783
ms.date: 12/05/2018
ms.keywords: DhcpServerQueryDnsRegCredentials, DhcpServerQueryDnsRegCredentials function [DHCP], dhcp.dhcpserverquerydnsregcredentials, dhcpsapi/DhcpServerQueryDnsRegCredentials
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
 - DhcpServerQueryDnsRegCredentials
 - dhcpsapi/DhcpServerQueryDnsRegCredentials
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
 - DhcpServerQueryDnsRegCredentials
---

# DhcpServerQueryDnsRegCredentials function


## -description

The <b>DhcpServerQueryDnsRegCredentials</b> function retrieves the current Domain Name System (DNS) credentials used by the DHCP server for client dynamic DNS registration.

## -parameters

### -param ServerIpAddress [in]

<a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-type-definitions">DHCP_SRV_HANDLE</a> that specifies the RPC binding to the DHCP server that will be queried.

### -param UnameSize [in]

Unsigned 32-bit integer that indicates the size, in bytes, to allocate for the data returned in the <i>Uname</i> buffer.

### -param Uname [out]

Pointer to a null-terminated Unicode string that contains the user name for the DNS server credentials. The size of this value cannot be larger than the size specified in <i>UnameSize</i>.

### -param DomainSize [in]

Unsigned 32-bit integer that indicates the size, in bytes, to allocate for the data returned in the <i>Domain</i> buffer.

### -param Domain [out]

Pointer to a null-terminated Unicode string that contains the domain name for the DNS server credentials. The size of this value cannot be larger than the size specified in <i>DomainSize</i>.

## -returns

This function returns <b>ERROR_SUCCESS</b> upon a successful call. Otherwise, it returns one of the <a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-api-error-codes">DHCP Server Management API Error Codes</a>.

## -remarks

DNS credentials can be set on the DHCP server by calling the <a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpserversetdnsregcredentialsv5">DhcpServerSetDnsRegCredentialsV5</a> function.

## -see-also

<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpserversetdnsregcredentialsv5">DhcpServerSetDnsRegCredentialsV5</a>