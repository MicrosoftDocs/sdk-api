---
UID: NN:searchapi.ISearchCrawlScopeManager
title: ISearchCrawlScopeManager
author: windows-sdk-content
description: Provides methods that notify the search engine of containers to crawl and/or watch, and items under those containers to include or exclude when crawling or watching.
old-location: search\_search_ISearchCrawlScopeManager.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\crawlscope\isearchcrawlscopemanager\isearchcrawlscopemanager.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: ISearchCrawlScopeManager, ISearchCrawlScopeManager interface [search], ISearchCrawlScopeManager interface [search],described, _search_ISearchCrawlScopeManager, search._search_ISearchCrawlScopeManager, searchapi/ISearchCrawlScopeManager
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
---

# ISearchCrawlScopeManager interface


## -description


Provides methods that notify the search engine of containers to crawl and/or watch, and items under those containers to include or exclude when crawling or watching.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISearchCrawlScopeManager</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ISearchCrawlScopeManager</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/948549da-7179-4f8d-956e-4daf20f8c65a">AddDefaultScopeRule</a>
</td>
<td align="left" width="63%">
Adds a URL as the default scope for this rule.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7aeabed7-0799-4eda-b806-d10365fa9dd4">AddHierarchicalScope</a>
</td>
<td align="left" width="63%">
Adds a hierarchical scope to the search engine.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6ce5e2c5-0c33-42a0-8807-eb64881b03af">AddRoot</a>
</td>
<td align="left" width="63%">
Adds a new search root to the search engine.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/100bf0b4-553c-4ecd-a40d-ee2948f2c4d5">AddUserScopeRule</a>
</td>
<td align="left" width="63%">
Adds a new crawl scope rule when the user creates a new rule or adds a URL to be indexed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/97f987ed-d6c3-4df2-b7b9-147945674a08">EnumerateRoots</a>
</td>
<td align="left" width="63%">
Returns an enumeration of all the roots of which this instance of the <b>ISearchCrawlScopeManager</b> is aware.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cb977157-5bce-48a8-afe5-7b6bbde17bb5">EnumerateScopeRules</a>
</td>
<td align="left" width="63%">
Returns an enumeration of all the scope rules of which this instance of the <b>ISearchCrawlScopeManager</b> interface is aware.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4a9228d3-f3c1-4bc1-ad21-d395bfe55b22">GetParentScopeVersionId</a>
</td>
<td align="left" width="63%">
Gets the version ID of the parent inclusion URL.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f8e7b10a-e9bc-401d-a79d-e38172c9fc1c">HasChildScopeRule</a>
</td>
<td align="left" width="63%">
Identifies whether a given URL has a child rule in scope.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ae0418f7-5f65-4a15-bf16-4e67645e0bad">HasParentScopeRule</a>
</td>
<td align="left" width="63%">
Identifies whether a given URL has a parent rule in scope.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bea05afa-3692-4f61-a25f-abf88357f25a">IncludedInCrawlScope</a>
</td>
<td align="left" width="63%">
Retrieves an indicator of whether the specified URL is included in the crawl scope.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/018c240b-491c-4974-8059-ee7331672e6b">IncludedInCrawlScopeEx</a>
</td>
<td align="left" width="63%">
Retrieves an indicator of whether and why the specified URL is included in the crawl scope.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c0ab627c-c7d3-4d6d-8c55-dea19c24a528">RemoveDefaultScopeRule</a>
</td>
<td align="left" width="63%">
Removes a default scope rule from the search engine.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/507281fd-2b93-45d3-9b50-297f3e771938">RemoveRoot</a>
</td>
<td align="left" width="63%">
Removes a search root from the search engine.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6ccc1dec-f97b-4959-8c73-2b47bc194ee3">RemoveScopeRule</a>
</td>
<td align="left" width="63%">
Removes a scope rule from the search engine.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b12e3eca-e151-466f-ba7a-7c3d91e4aed1">RevertToDefaultScopes</a>
</td>
<td align="left" width="63%">
Reverts to the default scopes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f9619acd-8b4a-4f43-869b-ea8b05cfefc6">SaveAll</a>
</td>
<td align="left" width="63%">
Commits all changes to the search engine.
        

</td>
</tr>
</table> 


## -remarks



<b>Windows 7 and later</b>: the CrawlScopeCommandLine code sample, available on <a href="http://go.microsoft.com/fwlink/p/?linkid=155654">Code Gallery</a> and the <a href="http://go.microsoft.com/fwlink/p/?linkid=129787">Windows 7 SDK</a>, demonstrates how to define command line options for Crawl Scope Manager (CSM) indexing operations.
      




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/cfba12eb-4123-4b57-8311-d4fc8f9f514e">The Indexing Process</a>



<a href="https://msdn.microsoft.com/7d65d00a-7294-4718-b593-89394b2e416f">Using the Crawl Scope Manager</a>
 

 

