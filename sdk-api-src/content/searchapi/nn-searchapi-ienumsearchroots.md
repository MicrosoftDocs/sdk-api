---
UID: NN:searchapi.IEnumSearchRoots
title: IEnumSearchRoots (searchapi.h)
description: Provides methods to enumerate the search roots of a catalog, for example, SystemIndex.
helpviewer_keywords: ["IEnumSearchRoots","IEnumSearchRoots interface [search]","IEnumSearchRoots interface [search]","described","_search_IEnumSearchRoots","search._search_IEnumSearchRoots","searchapi/IEnumSearchRoots"]
old-location: search\_search_IEnumSearchRoots.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\crawlscope\ienumsearchroots\ienumsearchroots.htm
ms.date: 12/05/2018
ms.keywords: IEnumSearchRoots, IEnumSearchRoots interface [search], IEnumSearchRoots interface [search],described, _search_IEnumSearchRoots, search._search_IEnumSearchRoots, searchapi/IEnumSearchRoots
f1_keywords:
- searchapi/IEnumSearchRoots
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
- COM
api_location:
- Searchapi.h
api_name:
- IEnumSearchRoots
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
---

# IEnumSearchRoots interface


## -description


Provides methods to enumerate the search roots of a catalog, for example, SystemIndex.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumSearchRoots</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumSearchRoots</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumSearchRoots</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nf-searchapi-ienumsearchroots-clone">Clone</a>
</td>
<td align="left" width="63%">
Creates a copy of the <b>IEnumSearchRoots</b> object with the same contents and state as the current one.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nf-searchapi-ienumsearchroots-next">Next</a>
</td>
<td align="left" width="63%">
Retrieves the specified number of <a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nn-searchapi-isearchroot">ISearchRoot</a> elements.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nf-searchapi-ienumsearchroots-reset">Reset</a>
</td>
<td align="left" width="63%">
Moves the internal counter to the beginning of the list so a subsequent call to <a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nf-searchapi-ienumsearchroots-next">IEnumSearchRoots::Next</a> retrieves from the beginning.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nf-searchapi-ienumsearchroots-skip">Skip</a>
</td>
<td align="left" width="63%">
Skips the specified number of elements.
        

</td>
</tr>
</table> 


## -remarks

For a sample that demonstrates how to define command line options for Crawl Scope Manager (CSM) indexing operations, see the [CrawlScopeCommandLine](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/CrawlScopeCommandLine) code sample.
        




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/search/-search-3x-wds-extidx-csm">Using the Crawl Scope Manager</a>
 

 

