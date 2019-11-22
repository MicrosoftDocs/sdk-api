---
UID: NF:dhcpsapi.DhcpServerSetDnsRegCredentialsV5
title: DhcpServerSetDnsRegCredentialsV5 function (dhcpsapi.h)

description: Sets the credentials used by the DHCP server to create Domain Name System (DNS) registrations for the DHCP client lease record.
old-location: dhcp\dhcpserversetdnsregcredentialsv5.htm
tech.root: DHCP
ms.assetid: 7fed2635-43a6-417a-996f-fff8d0692924

ms.date: 12/05/2018
ms.keywords: DhcpServerSetDnsRegCredentialsV5, DhcpServerSetDnsRegCredentialsV5 function [DHCP], dhcp.dhcpserversetdnsregcredentialsv5, dhcpsapi/DhcpServerSetDnsRegCredentialsV5
ms.topic: function
f1_keywords: 
 - "dhcpsapi/DhcpServerSetDnsRegCredentialsV5"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Dhcpsapi.dll
api_name:
 - DhcpServerSetDnsRegCredentialsV5
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DhcpServerSetDnsRegCredentialsV5 function


## -description


The <b>DhcpServerSetDnsRegCredentialsV5</b> function sets the credentials used by the DHCP server to create Domain Name System (DNS) registrations for the DHCP client lease record.


## -parameters




### -param ServerIpAddress [in]


<a href="https://docs.microsoft.com/previous-versions/windows/desktop/dhcp/dhcp-server-management-type-definitions">DHCP_SRV_HANDLE</a> that specifies the RPC binding to the DHCP server  on which the DNS credentials will be set.


### -param Uname [in]

Pointer to a null-terminated Unicode string that specifies the user name for the DNS credentials.


### -param Domain [in]

Pointer to a null-terminated Unicode string that specifies the domain name for the DNS credentials.


### -param Passwd [in]

Pointer to a null-terminated   Unicode string that specifies the password for the DNS credentials. The password can be unencrypted.


## -returns



This function returns <b>ERROR_SUCCESS</b> upon a successful call. Otherwise, it returns one of the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/dhcp/dhcp-server-management-api-error-codes">DHCP Server Management API Error Codes</a>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpserverquerydnsregcredentials">DhcpServerQueryDnsRegCredentials</a>
 

 

