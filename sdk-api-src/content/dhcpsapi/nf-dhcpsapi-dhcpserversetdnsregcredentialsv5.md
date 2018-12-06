---
UID: NF:dhcpsapi.DhcpServerSetDnsRegCredentialsV5
title: DhcpServerSetDnsRegCredentialsV5 function
author: windows-sdk-content
description: Sets the credentials used by the DHCP server to create Domain Name System (DNS) registrations for the DHCP client lease record.
old-location: dhcp\dhcpserversetdnsregcredentialsv5.htm
tech.root: DHCP
ms.assetid: 7fed2635-43a6-417a-996f-fff8d0692924
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DhcpServerSetDnsRegCredentialsV5, DhcpServerSetDnsRegCredentialsV5 function [DHCP], dhcp.dhcpserversetdnsregcredentialsv5, dhcpsapi/DhcpServerSetDnsRegCredentialsV5
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DhcpServerSetDnsRegCredentialsV5 function


## -description


The <b>DhcpServerSetDnsRegCredentialsV5</b> function sets the credentials used by the DHCP server to create Domain Name System (DNS) registrations for the DHCP client lease record.


## -parameters




### -param ServerIpAddress [in]


<a href="https://msdn.microsoft.com/8e29f488-2978-43dd-b7ba-edad2e3e4b29">DHCP_SRV_HANDLE</a> that specifies the RPC binding to the DHCP server  on which the DNS credentials will be set.


### -param Uname [in]

Pointer to a null-terminated Unicode string that specifies the user name for the DNS credentials.


### -param Domain [in]

Pointer to a null-terminated Unicode string that specifies the domain name for the DNS credentials.


### -param Passwd [in]

Pointer to a null-terminated   Unicode string that specifies the password for the DNS credentials. The password can be unencrypted.


## -returns



This function returns <b>ERROR_SUCCESS</b> upon a successful call. Otherwise, it returns one of the <a href="https://msdn.microsoft.com/6370313f-d7db-4ff1-b0e0-7fa47474facb">DHCP Server Management API Error Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/773cbfef-1dc5-4d44-9997-591acbfb3783">DhcpServerQueryDnsRegCredentials</a>
 

 

