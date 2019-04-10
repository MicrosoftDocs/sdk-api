---
UID: NF:windns.DnsReleaseContextHandle
title: DnsReleaseContextHandle function (windns.h)
author: windows-sdk-content
description: The DnsReleaseContextHandle function releases memory used to store the credentials of a specific account.
old-location: dns\dnsreleasecontexthandle.htm
tech.root: DNS
ms.assetid: 08a5fa73-4583-4e87-bddb-09bfbfe1b36f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DnsReleaseContextHandle, DnsReleaseContextHandle function [DNS], _dns_dnsreleasecontexthandle, dns.dnsreleasecontexthandle, windns/DnsReleaseContextHandle
ms.topic: function
req.header: windns.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
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
 - DnsReleaseContextHandle
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DnsReleaseContextHandle function


## -description


The 
<b>DnsReleaseContextHandle</b> function releases memory used to store the credentials of a specific account.


## -parameters




### -param hContext [in]

The credentials handle of a specific account.


## -returns



This function does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/ab7b96a5-346f-4e01-bb2a-885f44764590">DNS_RECORD</a>



<a href="https://msdn.microsoft.com/9a820165-2f78-44f4-b49f-dc7a2b6fb4e5">DnsAcquireContextHandle</a>
 

 

