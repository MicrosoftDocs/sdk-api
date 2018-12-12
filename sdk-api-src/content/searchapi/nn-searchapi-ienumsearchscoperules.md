---
UID: NN:searchapi.IEnumSearchScopeRules
title: IEnumSearchScopeRules
author: windows-sdk-content
description: Enumerates scope rules.
old-location: search\_search_IEnumSearchScopeRules.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\crawlscope\ienumsearchscoperules\ienumsearchscoperules.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IEnumSearchScopeRules, IEnumSearchScopeRules interface [search], IEnumSearchScopeRules interface [search],described, _search_IEnumSearchScopeRules, search._search_IEnumSearchScopeRules, searchapi/IEnumSearchScopeRules
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: searchapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Searchapi.idl
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
 - COM
api_location:
 - Searchapi.h
api_name:
 - IEnumSearchScopeRules
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnumSearchScopeRules interface


## -description


Enumerates scope rules.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumSearchScopeRules</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IEnumSearchScopeRules</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumSearchScopeRules</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/17c99d21-438f-40ff-ac6f-50f3ca6c91ee">Clone</a>
</td>
<td align="left" width="63%">
Creates a copy of this <b>IEnumSearchScopeRules</b> object with the same contents and state as the current one.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ef4472f1-348d-4545-8c8f-852a587e8096">Next</a>
</td>
<td align="left" width="63%">
Retrieves the specified number of <a href="https://msdn.microsoft.com/ace8d4f8-ffe0-45ff-8ba4-691efad23013">ISearchScopeRule</a> elements.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/afa73ad9-a697-4ad8-bb2f-0501d6046325">Reset</a>
</td>
<td align="left" width="63%">
Moves the internal counter to the beginning of the list so that a subsequent call to <a href="https://msdn.microsoft.com/ef4472f1-348d-4545-8c8f-852a587e8096">IEnumSearchScopeRules::Next</a> retrieves from the beginning.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/53889c73-3680-4222-9f2b-e41759a694ea">Skip</a>
</td>
<td align="left" width="63%">
Skips the specified number of elements.
        

</td>
</tr>
</table> 


## -remarks



<b>Windows 7 and later</b>: the CrawlScopeCommandLine code sample, available on <a href="http://go.microsoft.com/fwlink/p/?linkid=155654">Code Gallery</a> and the <a href="http://go.microsoft.com/fwlink/p/?linkid=129787">Windows 7 SDK</a>, demonstrates how to define command line options for Crawl Scope Manager (CSM) indexing operations.
      




## -see-also




<a href="https://msdn.microsoft.com/7d65d00a-7294-4718-b593-89394b2e416f">Using the Crawl Scope Manager</a>
 

 

