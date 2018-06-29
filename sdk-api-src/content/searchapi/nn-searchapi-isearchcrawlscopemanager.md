---
UID: NN:searchapi.ISearchCrawlScopeManager
title: ISearchCrawlScopeManager
author: windows-sdk-content
description: Provides methods that notify the search engine of containers to crawl and/or watch, and items under those containers to include or exclude when crawling or watching.
old-location: search\_search_ISearchCrawlScopeManager.htm
old-project: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\crawlscope\isearchcrawlscopemanager\isearchcrawlscopemanager.htm
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: ISearchCrawlScopeManager, ISearchCrawlScopeManager interface [search], ISearchCrawlScopeManager interface [search],described, _search_ISearchCrawlScopeManager, search._search_ISearchCrawlScopeManager, searchapi/ISearchCrawlScopeManager
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: ROWSETEVENT_TYPE
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
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
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
<a href="https://msdn.microsoft.com/library/Bb266481(v=VS.85).aspx">AddDefaultScopeRule</a>
</td>
<td align="left" width="63%">
Adds a URL as the default scope for this rule.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Bb266482(v=VS.85).aspx">AddHierarchicalScope</a>
</td>
<td align="left" width="63%">

            Adds a hierarchical scope to the search engine.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Bb266483(v=VS.85).aspx">AddRoot</a>
</td>
<td align="left" width="63%">

            Adds a new search root to the search engine.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Bb266484(v=VS.85).aspx">AddUserScopeRule</a>
</td>
<td align="left" width="63%">
Adds a new crawl scope rule when the user creates a new rule or adds a URL to be indexed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Bb266485(v=VS.85).aspx">EnumerateRoots</a>
</td>
<td align="left" width="63%">

            Returns an enumeration of all the roots of which this instance of the <b>ISearchCrawlScopeManager</b> is aware.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Bb266486(v=VS.85).aspx">EnumerateScopeRules</a>
</td>
<td align="left" width="63%">

          Returns an enumeration of all the scope rules of which this instance of the <b>ISearchCrawlScopeManager</b> interface is aware.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Bb266487(v=VS.85).aspx">GetParentScopeVersionId</a>
</td>
<td align="left" width="63%">
Gets the version ID of the parent inclusion URL.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Bb266488(v=VS.85).aspx">HasChildScopeRule</a>
</td>
<td align="left" width="63%">
Identifies whether a given URL has a child rule in scope.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Bb266489(v=VS.85).aspx">HasParentScopeRule</a>
</td>
<td align="left" width="63%">
Identifies whether a given URL has a parent rule in scope.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Bb266490(v=VS.85).aspx">IncludedInCrawlScope</a>
</td>
<td align="left" width="63%">

            Retrieves an indicator of whether the specified URL is included in the crawl scope.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Bb266491(v=VS.85).aspx">IncludedInCrawlScopeEx</a>
</td>
<td align="left" width="63%">
Retrieves an indicator of whether and why the specified URL is included in the crawl scope.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Bb266493(v=VS.85).aspx">RemoveDefaultScopeRule</a>
</td>
<td align="left" width="63%">
Removes a default scope rule from the search engine.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Bb266494(v=VS.85).aspx">RemoveRoot</a>
</td>
<td align="left" width="63%">

          Removes a search root from the search engine.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Bb266495(v=VS.85).aspx">RemoveScopeRule</a>
</td>
<td align="left" width="63%">
Removes a scope rule from the search engine.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Bb266496(v=VS.85).aspx">RevertToDefaultScopes</a>
</td>
<td align="left" width="63%">
Reverts to the default scopes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Bb266497(v=VS.85).aspx">SaveAll</a>
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



<a href="https://msdn.microsoft.com/library/Cc678933(v=VS.85).aspx">The Indexing Process</a>



<a href="https://msdn.microsoft.com/library/Bb266541(v=VS.85).aspx">Using the Crawl Scope Manager</a>
 

 

