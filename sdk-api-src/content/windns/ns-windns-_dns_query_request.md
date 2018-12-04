---
UID: NS:windns._DNS_QUERY_REQUEST
title: "_DNS_QUERY_REQUEST"
author: windows-sdk-content
description: The DNS_QUERY_REQUEST structure contains the DNS query parameters used in a call to DnsQueryEx.
old-location: dns\dns_query_request.htm
tech.root: dns
ms.assetid: 9C382800-DE71-4481-AC8D-9F89D6F59EE6
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: "*PDNS_QUERY_REQUEST, DNS_QUERY_REQUEST, DNS_QUERY_REQUEST structure [DNS], DNS_QUERY_REQUEST_VERSION1, PDNS_QUERY_REQUEST, PDNS_QUERY_REQUEST structure pointer [DNS], _DNS_QUERY_REQUEST, dns.dns_query_request, windns/DNS_QUERY_REQUEST, windns/PDNS_QUERY_REQUEST"
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
 - DNS_QUERY_REQUEST
product: Windows
targetos: Windows
req.typenames: DNS_QUERY_REQUEST, *PDNS_QUERY_REQUEST
req.redist: 
---

# _DNS_QUERY_REQUEST structure


## -description


The <b>DNS_QUERY_REQUEST</b> structure contains the DNS query parameters used in a call to <a href="https://msdn.microsoft.com/22664B9A-5010-42E7-880B-8D5B16A9F2DC">DnsQueryEx</a>.


## -struct-fields




### -field Version

The structure version must be one of the following:



#### DNS_QUERY_REQUEST_VERSION1 (1)


### -field QueryName

A pointer to a string that represents the DNS name to query.

<div class="alert"><b>Note</b>  If <b>QueryName</b> is NULL, the query is for the local machine name.</div>
<div> </div>

### -field QueryType

A value that represents the Resource Record (RR) <a href="https://msdn.microsoft.com/95bc9193-7962-498a-9abd-c4718ac35f0f">DNS Record Type</a> that is queried. <b>QueryType</b> determines the format of data pointed to by <b>pQueryRecords</b> returned in the <a href="https://msdn.microsoft.com/03EB1DC2-FAB0-45C5-B438-E8FFDD218F09">DNS_QUERY_RESULT</a> structure. For example, if the value of <b>wType</b> is <b>DNS_TYPE_A</b>, the format of data pointed to by <b>pQueryRecords</b> is <a href="https://msdn.microsoft.com/0fd21930-1319-4ae7-b46f-2b744f4faae9">DNS_A_DATA</a>.


### -field QueryOptions

A value that contains a bitmap of <a href="https://msdn.microsoft.com/95bc9193-7962-498a-9abd-c4718ac35f0f">DNS Query  Options</a> to use in the DNS query. Options can be combined and all options override <b>DNS_QUERY_STANDARD</b>


### -field pDnsServerList

A pointer to a <a href="https://msdn.microsoft.com/5FD7F28B-D1A6-4731-ACB9-A7BB23CC1FB4">DNS_ADDR_ARRAY</a> structure that contains a list of DNS servers to use in the query.


### -field InterfaceIndex

A value that contains the interface index over which the query is sent. If <b>InterfaceIndex</b> is 0, all interfaces will be considered.


### -field pQueryCompletionCallback

A pointer to a <a href="https://msdn.microsoft.com/35D78208-FFC1-48B0-8267-EE583DE2D783">DNS_QUERY_COMPLETION_ROUTINE</a> callback that is used to return the results of an asynchronous query from a  call to <a href="https://msdn.microsoft.com/22664B9A-5010-42E7-880B-8D5B16A9F2DC">DnsQueryEx</a>.

<div class="alert"><b>Note</b>  If NULL, <a href="https://msdn.microsoft.com/22664B9A-5010-42E7-880B-8D5B16A9F2DC">DnsQueryEx</a> is called synchronously.</div>
<div> </div>

### -field pQueryContext

A pointer to a user context.


## -see-also




<a href="https://msdn.microsoft.com/543C6F9B-3200-44F6-A2B7-A5C7F5A927DB">DNS_QUERY_CANCEL</a>



<a href="https://msdn.microsoft.com/35D78208-FFC1-48B0-8267-EE583DE2D783">DNS_QUERY_COMPLETION_ROUTINE</a>



<a href="https://msdn.microsoft.com/03EB1DC2-FAB0-45C5-B438-E8FFDD218F09">DNS_QUERY_RESULT</a>



<a href="https://msdn.microsoft.com/E5F422AA-D4E6-4F9F-A57C-608CE9317658">DnsCancelQuery</a>



<a href="https://msdn.microsoft.com/3d810b76-cea1-4904-9b5a-c2566b332c2c">DnsQuery</a>



<a href="https://msdn.microsoft.com/22664B9A-5010-42E7-880B-8D5B16A9F2DC">DnsQueryEx</a>
 

 

