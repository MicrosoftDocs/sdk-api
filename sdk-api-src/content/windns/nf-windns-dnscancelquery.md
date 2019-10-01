---
UID: NF:windns.DnsCancelQuery
title: DnsCancelQuery function (windns.h)
author: windows-sdk-content
description: The DnsCancelQuery function can be used to cancel a pending query to the DNS namespace.
old-location: dns\dnscancelquery.htm
tech.root: DNS
ms.assetid: E5F422AA-D4E6-4F9F-A57C-608CE9317658
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DnsCancelQuery, DnsCancelQuery function [DNS], dns.dnscancelquery, windns/DnsCancelQuery
ms.topic: function
f1_keywords:
- windns/DnsCancelQuery
req.header: windns.h
req.include-header: 
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
- DnsCancelQuery
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DnsCancelQuery function


## -description


The <b>DnsCancelQuery</b> function can be used to cancel a pending query to the DNS namespace.


## -parameters




### -param pCancelHandle [in]

A pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/windns/ns-windns-dns_query_cancel">DNS_QUERY_CANCEL</a> structure used to cancel an asynchronous DNS query. The structure must have been returned in the <i>pCancelHandle</i> parameter of a previous call to <a href="https://docs.microsoft.com/windows/desktop/api/windns/nf-windns-dnsqueryex">DnsQueryEx</a>.


## -returns



Returns success confirmation upon successful completion. Otherwise, it returns the appropriate DNS-specific error code as defined in Winerror.h.




## -remarks



<b>DnsCancelQuery</b> does not wait for a query to complete before cancelling. Therefore,
    applications should track pending queries through their <a href="https://docs.microsoft.com/windows/desktop/api/windns/nc-windns-dns_query_completion_routine">DNS_QUERY_COMPLETION_ROUTINE</a> DNS callbacks.

<i>pCancelHandle</i> is valid until the <a href="https://docs.microsoft.com/windows/desktop/api/windns/nc-windns-dns_query_completion_routine">DNS_QUERY_COMPLETION_ROUTINE</a> DNS callback is invoked and <b>DnsCancelQuery</b> completes.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/windns/nc-windns-dns_query_completion_routine">DNS_QUERY_COMPLETION_ROUTINE</a>



<a href="https://docs.microsoft.com/windows/desktop/api/windns/ns-windns-dns_query_request">DNS_QUERY_REQUEST</a>



<a href="https://docs.microsoft.com/windows/desktop/api/windns/ns-windns-dns_query_result">DNS_QUERY_RESULT</a>



<a href="https://docs.microsoft.com/windows/desktop/api/windns/nf-windns-dnsquery_a">DnsQuery</a>



<a href="https://docs.microsoft.com/windows/desktop/api/windns/nf-windns-dnsqueryex">DnsQueryEx</a>
 

 

