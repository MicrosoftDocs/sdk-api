---
UID: NC:windns.DNS_QUERY_COMPLETION_ROUTINE
title: DNS_QUERY_COMPLETION_ROUTINE
author: windows-driver-content
description: The DNS_QUERY_COMPLETION_ROUTINE callback is used to asynchronously return the results of a DNS query.
old-location: dns\dns_query_completion_routine.htm
old-project: DNS
ms.assetid: 35D78208-FFC1-48B0-8267-EE583DE2D783
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: DNS_QUERY_COMPLETION_ROUTINE, DNS_QUERY_COMPLETION_ROUTINE callback function [DNS], dns.dns_query_completion_routine, windns/DNS_QUERY_COMPLETION_ROUTINE
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
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
req.typenames: RECTL, *PRECTL, *LPRECTL
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	Windns.h
api_name:
-	DNS_QUERY_COMPLETION_ROUTINE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# DNS_QUERY_COMPLETION_ROUTINE callback


## -description


The <b>DNS_QUERY_COMPLETION_ROUTINE</b> callback is used to asynchronously return the results of a DNS query.


## -parameters




### -param pQueryContext [in]

A pointer to a user context.


### -param pQueryResults [in, out]

A pointer to a <a href="https://msdn.microsoft.com/03EB1DC2-FAB0-45C5-B438-E8FFDD218F09">DNS_QUERY_RESULT</a> structure that contains the DNS query results from a call to <a href="https://msdn.microsoft.com/22664B9A-5010-42E7-880B-8D5B16A9F2DC">DnsQueryEx</a>.


## -returns



This callback function does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/543C6F9B-3200-44F6-A2B7-A5C7F5A927DB">DNS_QUERY_CANCEL</a>



<a href="https://msdn.microsoft.com/9C382800-DE71-4481-AC8D-9F89D6F59EE6">DNS_QUERY_REQUEST</a>



<a href="https://msdn.microsoft.com/03EB1DC2-FAB0-45C5-B438-E8FFDD218F09">DNS_QUERY_RESULT</a>



<a href="https://msdn.microsoft.com/E5F422AA-D4E6-4F9F-A57C-608CE9317658">DnsCancelQuery</a>



<a href="https://msdn.microsoft.com/22664B9A-5010-42E7-880B-8D5B16A9F2DC">DnsQueryEx</a>
 

 

