---
UID: NS:windns._DNS_QUERY_RESULT
title: "_DNS_QUERY_RESULT"
author: windows-sdk-content
description: A DNS_QUERY_RESULT structure contains the DNS query results returned from a call to DnsQueryEx.
old-location: dns\dns_query_result.htm
tech.root: DNS
ms.assetid: 03EB1DC2-FAB0-45C5-B438-E8FFDD218F09
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: "*PDNS_QUERY_RESULT, DNS_QUERY_REQUEST_VERSION1, DNS_QUERY_RESULT, DNS_QUERY_RESULT structure [DNS], PDNS_QUERY_RESULT, PDNS_QUERY_RESULT structure pointer [DNS], _DNS_QUERY_RESULT, dns.dns_query_result, windns/DNS_QUERY_RESULT, windns/PDNS_QUERY_RESULT"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Windns.h
api_name:
 - DNS_QUERY_RESULT
product: Windows
targetos: Windows
req.typenames: DNS_QUERY_RESULT, *PDNS_QUERY_RESULT
req.redist: 
---

# _DNS_QUERY_RESULT structure


## -description


A <b>DNS_QUERY_RESULT</b>  structure contains the DNS query results returned from a call to <a href="https://msdn.microsoft.com/22664B9A-5010-42E7-880B-8D5B16A9F2DC">DnsQueryEx</a>.


## -struct-fields




### -field Version

The structure version must be one of the following:



#### DNS_QUERY_REQUEST_VERSION1 (1)


### -field QueryStatus

The return status of the call to <a href="https://msdn.microsoft.com/22664B9A-5010-42E7-880B-8D5B16A9F2DC">DnsQueryEx</a>. 

If the query was completed asynchronously and this structure was returned directly from <a href="https://msdn.microsoft.com/22664B9A-5010-42E7-880B-8D5B16A9F2DC">DnsQueryEx</a>, <b>QueryStatus</b> contains <b>DNS_REQUEST_PENDING</b>.

If the query was completed synchronously or if this structure was returned by the <a href="https://msdn.microsoft.com/35D78208-FFC1-48B0-8267-EE583DE2D783">DNS_QUERY_COMPLETION_ROUTINE</a> DNS callback, <b>QueryStatus</b> contains ERROR_SUCCESS if successful or the appropriate DNS-specific error code as defined in Winerror.h.


### -field QueryOptions

A value that contains a bitmap of <a href="https://msdn.microsoft.com/95bc9193-7962-498a-9abd-c4718ac35f0f">DNS Query  Options</a> that were used in the DNS query. Options can be combined and all options override <b>DNS_QUERY_STANDARD</b>


### -field pQueryRecords

A pointer to a <a href="https://msdn.microsoft.com/ab7b96a5-346f-4e01-bb2a-885f44764590">DNS_RECORD</a> structure.

If the query was completed asynchronously and this structure was returned directly from <a href="https://msdn.microsoft.com/22664B9A-5010-42E7-880B-8D5B16A9F2DC">DnsQueryEx</a>, <b>pQueryRecords</b> is NULL.

If the query was completed synchronously or if this structure was returned by the <a href="https://msdn.microsoft.com/35D78208-FFC1-48B0-8267-EE583DE2D783">DNS_QUERY_COMPLETION_ROUTINE</a> DNS callback, <b>pQueryRecords</b> contains a list of Resource Records (RR) that comprise the response.

<div class="alert"><b>Note</b>  Applications must free returned RR sets with the <a href="https://msdn.microsoft.com/fc4c0cb4-646f-4946-8f07-b5a858f7064a">DnsRecordListFree</a> function.</div>
<div> </div>

### -field Reserved

 




#### - reserved

This value is reserved for future use and must be <b>NULL</b>.


## -see-also




<a href="https://msdn.microsoft.com/543C6F9B-3200-44F6-A2B7-A5C7F5A927DB">DNS_QUERY_CANCEL</a>



<a href="https://msdn.microsoft.com/35D78208-FFC1-48B0-8267-EE583DE2D783">DNS_QUERY_COMPLETION_ROUTINE</a>



<a href="https://msdn.microsoft.com/9C382800-DE71-4481-AC8D-9F89D6F59EE6">DNS_QUERY_REQUEST</a>
 

 

