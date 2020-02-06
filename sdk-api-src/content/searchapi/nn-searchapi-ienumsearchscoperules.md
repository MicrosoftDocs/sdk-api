---
UID: NN:searchapi.IEnumSearchScopeRules
title: IEnumSearchScopeRules (searchapi.h)
description: Enumerates scope rules.
old-location: search\_search_IEnumSearchScopeRules.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\crawlscope\ienumsearchscoperules\ienumsearchscoperules.htm
ms.date: 12/05/2018
ms.keywords: IEnumSearchScopeRules, IEnumSearchScopeRules interface [search], IEnumSearchScopeRules interface [search],described, _search_IEnumSearchScopeRules, search._search_IEnumSearchScopeRules, searchapi/IEnumSearchScopeRules
f1_keywords:
- searchapi/IEnumSearchScopeRules
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEnumSearchScopeRules interface


## -description


Enumerates scope rules.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumSearchScopeRules</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumSearchScopeRules</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nf-searchapi-ienumsearchscoperules-clone">Clone</a>
</td>
<td align="left" width="63%">
Creates a copy of this <b>IEnumSearchScopeRules</b> object with the same contents and state as the current one.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nf-searchapi-ienumsearchscoperules-next">Next</a>
</td>
<td align="left" width="63%">
Retrieves the specified number of <a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nn-searchapi-isearchscoperule">ISearchScopeRule</a> elements.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nf-searchapi-ienumsearchscoperules-reset">Reset</a>
</td>
<td align="left" width="63%">
Moves the internal counter to the beginning of the list so that a subsequent call to <a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nf-searchapi-ienumsearchscoperules-next">IEnumSearchScopeRules::Next</a> retrieves from the beginning.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nf-searchapi-ienumsearchscoperules-skip">Skip</a>
</td>
<td align="left" width="63%">
Skips the specified number of elements.
        

</td>
</tr>
</table> 


## -remarks



<b>Windows 7 and later</b>: the CrawlScopeCommandLine code sample, available on <a href="https://go.microsoft.com/fwlink/p/?linkid=155654">Code Gallery</a> and the <a href="https://go.microsoft.com/fwlink/p/?linkid=129787">Windows 7 SDK</a>, demonstrates how to define command line options for Crawl Scope Manager (CSM) indexing operations.
      




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/search/-search-3x-wds-extidx-csm">Using the Crawl Scope Manager</a>
 

 

