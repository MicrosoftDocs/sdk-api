---
UID: NN:searchapi.ISearchCrawlScopeManager
title: ISearchCrawlScopeManager (searchapi.h)
description: Provides methods that notify the search engine of containers to crawl and/or watch, and items under those containers to include or exclude when crawling or watching.
old-location: search\_search_ISearchCrawlScopeManager.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\crawlscope\isearchcrawlscopemanager\isearchcrawlscopemanager.htm
ms.date: 12/05/2018
ms.keywords: ISearchCrawlScopeManager, ISearchCrawlScopeManager interface [search], ISearchCrawlScopeManager interface [search],described, _search_ISearchCrawlScopeManager, search._search_ISearchCrawlScopeManager, searchapi/ISearchCrawlScopeManager
f1_keywords:
- searchapi/ISearchCrawlScopeManager
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
req.idl: Searchcrawlscopemanager.idl
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
- ISearchCrawlScopeManager
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
---

# ISearchCrawlScopeManager interface


## -description


Provides methods that notify the search engine of containers to crawl and/or watch, and items under those containers to include or exclude when crawling or watching.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISearchCrawlScopeManager</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISearchCrawlScopeManager</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISearchCrawlScopeManager</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nf-searchapi-isearchcrawlscopemanager-adddefaultscoperule">AddDefaultScopeRule</a>
</td>
<td align="left" width="63%">
Adds a URL as the default scope for this rule.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nf-searchapi-isearchcrawlscopemanager-addhierarchicalscope">AddHierarchicalScope</a>
</td>
<td align="left" width="63%">
Adds a hierarchical scope to the search engine.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nf-searchapi-isearchcrawlscopemanager-addroot">AddRoot</a>
</td>
<td align="left" width="63%">
Adds a new search root to the search engine.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nf-searchapi-isearchcrawlscopemanager-adduserscoperule">AddUserScopeRule</a>
</td>
<td align="left" width="63%">
Adds a new crawl scope rule when the user creates a new rule or adds a URL to be indexed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nf-searchapi-isearchcrawlscopemanager-enumerateroots">EnumerateRoots</a>
</td>
<td align="left" width="63%">
Returns an enumeration of all the roots of which this instance of the <b>ISearchCrawlScopeManager</b> is aware.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nf-searchapi-isearchcrawlscopemanager-enumeratescoperules">EnumerateScopeRules</a>
</td>
<td align="left" width="63%">
Returns an enumeration of all the scope rules of which this instance of the <b>ISearchCrawlScopeManager</b> interface is aware.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nf-searchapi-isearchcrawlscopemanager-getparentscopeversionid">GetParentScopeVersionId</a>
</td>
<td align="left" width="63%">
Gets the version ID of the parent inclusion URL.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nf-searchapi-isearchcrawlscopemanager-haschildscoperule">HasChildScopeRule</a>
</td>
<td align="left" width="63%">
Identifies whether a given URL has a child rule in scope.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nf-searchapi-isearchcrawlscopemanager-hasparentscoperule">HasParentScopeRule</a>
</td>
<td align="left" width="63%">
Identifies whether a given URL has a parent rule in scope.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nf-searchapi-isearchcrawlscopemanager-includedincrawlscope">IncludedInCrawlScope</a>
</td>
<td align="left" width="63%">
Retrieves an indicator of whether the specified URL is included in the crawl scope.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nf-searchapi-isearchcrawlscopemanager-includedincrawlscopeex">IncludedInCrawlScopeEx</a>
</td>
<td align="left" width="63%">
Retrieves an indicator of whether and why the specified URL is included in the crawl scope.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nf-searchapi-isearchcrawlscopemanager-removedefaultscoperule">RemoveDefaultScopeRule</a>
</td>
<td align="left" width="63%">
Removes a default scope rule from the search engine.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nf-searchapi-isearchcrawlscopemanager-removeroot">RemoveRoot</a>
</td>
<td align="left" width="63%">
Removes a search root from the search engine.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nf-searchapi-isearchcrawlscopemanager-removescoperule">RemoveScopeRule</a>
</td>
<td align="left" width="63%">
Removes a scope rule from the search engine.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nf-searchapi-isearchcrawlscopemanager-reverttodefaultscopes">RevertToDefaultScopes</a>
</td>
<td align="left" width="63%">
Reverts to the default scopes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nf-searchapi-isearchcrawlscopemanager-saveall">SaveAll</a>
</td>
<td align="left" width="63%">
Commits all changes to the search engine.
        

</td>
</tr>
</table> 


## -remarks



<b>Windows 7 and later</b>: the CrawlScopeCommandLine code sample, available on <a href="https://code.msdn.microsoft.com/windowssearch">Code Gallery</a> and the <a href="https://msdn.microsoft.com/windowsvista/bb980924.aspx">Windows 7 SDK</a>, demonstrates how to define command line options for Crawl Scope Manager (CSM) indexing operations.
      




## -see-also




<b>Conceptual</b>



<a href="https://docs.microsoft.com/windows/desktop/search/-search-indexing-process-overview">The Indexing Process</a>



<a href="https://docs.microsoft.com/windows/desktop/search/-search-3x-wds-extidx-csm">Using the Crawl Scope Manager</a>
 

 

