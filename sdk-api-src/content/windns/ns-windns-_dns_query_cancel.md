---
UID: NS:windns._DNS_QUERY_CANCEL
title: "_DNS_QUERY_CANCEL"
author: windows-sdk-content
description: A DNS_QUERY_CANCEL structure can be used to cancel an asynchronous DNS query.
old-location: dns\dns_query_cancel.htm
old-project: dns
ms.assetid: 543C6F9B-3200-44F6-A2B7-A5C7F5A927DB
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*PDNS_QUERY_CANCEL, DNS_QUERY_CANCEL, DNS_QUERY_CANCEL structure [DNS], PDNS_QUERY_CANCEL, PDNS_QUERY_CANCEL structure pointer [DNS], _DNS_QUERY_CANCEL, dns.dns_query_cancel, windns/DNS_QUERY_CANCEL, windns/PDNS_QUERY_CANCEL"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: windns.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.typenames: DNS_QUERY_CANCEL, *PDNS_QUERY_CANCEL
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Windns.h
api_name:
 - DNS_QUERY_CANCEL
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _DNS_QUERY_CANCEL structure


## -description


A <b>DNS_QUERY_CANCEL</b> structure can be used to cancel an asynchronous DNS query.


## -struct-fields




### -field Reserved

Contains a handle to the asynchronous query to cancel. Applications must not modify this value.


## -remarks



This structure is returned in the <i>pCancelHandle</i> parameter from a previous call to <a href="https://msdn.microsoft.com/22664B9A-5010-42E7-880B-8D5B16A9F2DC">DnsQueryEx</a>.




## -see-also




<a href="https://msdn.microsoft.com/35D78208-FFC1-48B0-8267-EE583DE2D783">DNS_QUERY_COMPLETION_ROUTINE</a>



<a href="https://msdn.microsoft.com/9C382800-DE71-4481-AC8D-9F89D6F59EE6">DNS_QUERY_REQUEST</a>



<a href="https://msdn.microsoft.com/03EB1DC2-FAB0-45C5-B438-E8FFDD218F09">DNS_QUERY_RESULT</a>
 

 

