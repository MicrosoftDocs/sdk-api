---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

