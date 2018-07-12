---
UID: NS:windns.DNS_PROXY_INFORMATION
title: DNS_PROXY_INFORMATION
author: windows-sdk-content
description: Contains the proxy information for a DNS server's name resolution policy table.
old-location: dns\dns_proxy_information.htm
old-project: dns
ms.assetid: cfe7653f-7e68-4e50-ba67-bd441f837ef8
ms.author: windowssdkdev
ms.date: 05/14/2018
ms.keywords: DNS_PROXY_INFORMATION, DNS_PROXY_INFORMATION structure [DNS], PDNS_PROXY_INFORMATION, PDNS_PROXY_INFORMATION structure pointer [DNS], dns.dns_proxy_information, windns/DNS_PROXY_INFORMATION, windns/PDNS_PROXY_INFORMATION
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: DNS_PROXY_INFORMATION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Windns.h
api_name:
 - DNS_PROXY_INFORMATION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# DNS_PROXY_INFORMATION structure


## -description


The <b>DNS_PROXY_INFORMATION</b> structure  contains the proxy information for a DNS server's name resolution policy table.


## -struct-fields




### -field version

A value that specifies the structure version. This value must be 1.


### -field proxyInformationType

A <a href="https://msdn.microsoft.com/983d38f3-3ee7-4df6-a9ff-f908f250020f">DNS_PROXY_INFORMATION_TYPE</a> enumeration that contains the proxy information type.


### -field proxyName

A pointer to a string that contains the proxy server name if <b>proxyInformationType</b> is <b>DNS_PROXY_INFORMATION_PROXY_NAME</b>. Otherwise, this member is ignored.

<div class="alert"><b>Note</b>  To free this string, use the 
<a href="https://msdn.microsoft.com/4c69d548-3bb5-4609-9fc5-3a829a285956">DnsFreeProxyName</a> function.</div>
<div> </div>

## -see-also




<a href="https://msdn.microsoft.com/636399be-43a5-4ddf-b652-f8efb81fbf42">DNS Structures</a>



<a href="https://msdn.microsoft.com/fdc8eb09-e071-4f03-974a-2b11a657ab18">DnsGetProxyInformation</a>
 

 

