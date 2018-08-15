---
UID: NF:windns.DnsFreeProxyName
title: DnsFreeProxyName function
author: windows-sdk-content
description: Frees memory allocated for the proxyName member of a DNS_PROXY_INFORMATION structure obtained using the DnsGetProxyInformation function.
old-location: dns\dnsfreeproxyname.htm
old-project: dns
ms.assetid: 4c69d548-3bb5-4609-9fc5-3a829a285956
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: DnsFreeProxyName, DnsFreeProxyName function [DNS], dns.dnsfreeproxyname, windns/DnsFreeProxyName
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: windns.h
req.include-header: 
req.redist: 
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
req.typenames: DNS_FREE_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Dnsapi.dll
api_name:
 - DnsFreeProxyName
product: Windows
targetos: Windows
req.lib: Dnsapi.lib
req.dll: Dnsapi.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# DnsFreeProxyName function


## -description


The 
<b>DnsFreeProxyName</b> function frees memory allocated for the <b>proxyName</b> member of a <a href="https://msdn.microsoft.com/cfe7653f-7e68-4e50-ba67-bd441f837ef8">DNS_PROXY_INFORMATION</a> structure obtained using the 
<a href="https://msdn.microsoft.com/fdc8eb09-e071-4f03-974a-2b11a657ab18">DnsGetProxyInformation</a> function.


## -parameters




### -param proxyName [in, out]

A pointer to the <b>proxyName</b> string to be freed.


## -returns



This function does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/9b3c1c20-5516-41de-b00f-b95736ff53f1">DNS Functions</a>
 

 

