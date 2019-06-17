---
UID: NF:windns.DnsFree
title: DnsFree function (windns.h)
author: windows-sdk-content
description: Frees memory allocated for DNS records that was obtained using the DnsQuery function.
old-location: dns\dnsfree.htm
tech.root: DNS
ms.assetid: 32baa672-2106-4c4a-972a-f7f79996b613
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DnsFree, DnsFree function [DNS], dns.dnsfree, windns/DnsFree
ms.topic: function
f1_keywords: ["windns/DnsFree"]
req.header: windns.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - DnsFree
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DnsFree function


## -description


The <b>DnsFree</b> function frees memory allocated for DNS records that was obtained using the 
<a href="https://docs.microsoft.com/windows/desktop/api/windns/nf-windns-dnsquery_a">DnsQuery</a> function.


## -parameters




### -param pData [in, out]

A pointer to the DNS data to be freed.


### -param FreeType [in]

A value that specifies the type of DNS data in <i>pData</i>. For more information and a list of values, see the <a href="https://docs.microsoft.com/windows/desktop/api/windns/ne-windns-__unnamed_enum_1">DNS_FREE_TYPE</a> enumeration.


## -returns



This function does not return a value.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/windns/ne-windns-__unnamed_enum_1">DNS_FREE_TYPE</a>
 

 

