---
UID: NF:windns.DnsGetProxyInformation
title: DnsGetProxyInformation function
author: windows-sdk-content
description: The DnsGetProxyInformation function returns the proxy information for a DNS server's name resolution policy table.
old-location: dns\dnsgetproxyinformation.htm
tech.root: DNS
ms.assetid: fdc8eb09-e071-4f03-974a-2b11a657ab18
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DnsGetProxyInformation, DnsGetProxyInformation function [DNS], dns.dnsgetproxyinformation, windns/DnsGetProxyInformation
ms.topic: function
req.header: windns.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
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
req.lib: Dnsapi.lib
req.dll: Dnsapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Dnsapi.dll
api_name:
 - DnsGetProxyInformation
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DnsGetProxyInformation function


## -description


The 
<b>DnsGetProxyInformation</b> function returns the proxy information for a DNS server's name resolution policy table.


## -parameters




### -param hostName [in]

A pointer to a string that represents the name of the DNS server whose proxy information is returned.


### -param proxyInformation [in, out]

A pointer to a <a href="https://msdn.microsoft.com/cfe7653f-7e68-4e50-ba67-bd441f837ef8">DNS_PROXY_INFORMATION</a> structure that contains the proxy information for <i>hostName</i>.


### -param defaultProxyInformation [in, out, optional]

A pointer to a <a href="https://msdn.microsoft.com/cfe7653f-7e68-4e50-ba67-bd441f837ef8">DNS_PROXY_INFORMATION</a> structure that contains the default proxy information for <i>hostName</i>. This proxy information is for the wildcard DNS policy.


### -param completionRoutine [in, optional]

Reserved. Do not use.


### -param completionContext [in, optional]

Reserved. Do not use.


## -returns



The 
<b>DnsGetProxyInformation</b> function returns the appropriate DNS-specific error code as defined in Winerror.h. The following are possible return values:




## -see-also




<a href="https://msdn.microsoft.com/9b3c1c20-5516-41de-b00f-b95736ff53f1">DNS Functions</a>
 

 

