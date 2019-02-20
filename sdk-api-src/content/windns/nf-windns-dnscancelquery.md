---
UID: NF:windns.DnsCancelQuery
title: DnsCancelQuery function
author: windows-sdk-content
description: The DnsCancelQuery function can be used to cancel a pending query to the DNS namespace.
old-location: dns\dnscancelquery.htm
tech.root: DNS
ms.assetid: E5F422AA-D4E6-4F9F-A57C-608CE9317658
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DnsCancelQuery, DnsCancelQuery function [DNS], dns.dnscancelquery, windns/DnsCancelQuery
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DnsCancelQuery function


## -description


The <b>DnsCancelQuery</b> function can be used to cancel a pending query to the DNS namespace.


## -parameters




### -param pCancelHandle [in]

A pointer to a <a href="https://msdn.microsoft.com/543C6F9B-3200-44F6-A2B7-A5C7F5A927DB">DNS_QUERY_CANCEL</a> structure used to cancel an asynchronous DNS query. The structure must have been returned in the <i>pCancelHandle</i> parameter of a previous call to <a href="https://msdn.microsoft.com/22664B9A-5010-42E7-880B-8D5B16A9F2DC">DnsQueryEx</a>.


## -returns



Returns success confirmation upon successful completion. Otherwise, it returns the appropriate DNS-specific error code as defined in Winerror.h.




## -remarks



<b>DnsCancelQuery</b> does not wait for a query to complete before cancelling. Therefore,
    applications should track pending queries through their <a href="https://msdn.microsoft.com/35D78208-FFC1-48B0-8267-EE583DE2D783">DNS_QUERY_COMPLETION_ROUTINE</a> DNS callbacks.

<i>pCancelHandle</i> is valid until the <a href="https://msdn.microsoft.com/35D78208-FFC1-48B0-8267-EE583DE2D783">DNS_QUERY_COMPLETION_ROUTINE</a> DNS callback is invoked and <b>DnsCancelQuery</b> completes.




## -see-also




<a href="https://msdn.microsoft.com/35D78208-FFC1-48B0-8267-EE583DE2D783">DNS_QUERY_COMPLETION_ROUTINE</a>



<a href="https://msdn.microsoft.com/9C382800-DE71-4481-AC8D-9F89D6F59EE6">DNS_QUERY_REQUEST</a>



<a href="https://msdn.microsoft.com/03EB1DC2-FAB0-45C5-B438-E8FFDD218F09">DNS_QUERY_RESULT</a>



<a href="https://msdn.microsoft.com/3d810b76-cea1-4904-9b5a-c2566b332c2c">DnsQuery</a>



<a href="https://msdn.microsoft.com/22664B9A-5010-42E7-880B-8D5B16A9F2DC">DnsQueryEx</a>
 

 

