---
UID: NN:searchapi.ISearchCrawlScopeManager2
title: ISearchCrawlScopeManager2
author: windows-sdk-content
description: Extends the functionality of the ISearchCrawlScopeManager interface.
old-location: search\_search_ISearchCrawlScopeManager2.htm
old-project: search
ms.assetid: VS|SEARCH|~\search\wds3x\reference\ifaces\crawlscope\isearchcrawlscopemanager2\isearchcrawlscopemanager2.htm
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: ISearchCrawlScopeManager2, ISearchCrawlScopeManager2 interface [search], ISearchCrawlScopeManager2 interface [search],described, _search_ISearchCrawlScopeManager2, search._search_ISearchCrawlScopeManager2, searchapi/ISearchCrawlScopeManager2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: searchapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - ISearchCrawlScopeManager2
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# ISearchCrawlScopeManager2 interface


## -description


Extends the functionality of the <a href="https://msdn.microsoft.com/8b731941-f1f6-402e-8cee-3c493e3c369d">ISearchCrawlScopeManager</a> interface. <b>ISearchCrawlScopeManager2</b> provides methods that notify the search engine of containers to crawl and/or watch, and items under those containers to include or exclude when crawling or watching.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISearchCrawlScopeManager2</b> interface inherits from <a href="https://msdn.microsoft.com/8b731941-f1f6-402e-8cee-3c493e3c369d">ISearchCrawlScopeManager</a>. <b>ISearchCrawlScopeManager2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISearchCrawlScopeManager2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7cdcd205-3f91-48bb-b831-444e55bd5e0e">GetVersion</a>
</td>
<td align="left" width="63%">
Causes file mapping to be mapped into the address space of the calling process, and informs clients if the state of the Crawl Scope Manager (CSM) has changed.

</td>
</tr>
</table> 


## -remarks



<b>Windows 7 and later</b>: the CrawlScopeCommandLine code sample, available on <a href="http://go.microsoft.com/fwlink/p/?linkid=155654">Code Gallery</a> and the <a href="http://go.microsoft.com/fwlink/p/?linkid=129787">Windows 7 SDK</a>, demonstrates how to define command line options for Crawl Scope Manager (CSM) indexing operations.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/8b731941-f1f6-402e-8cee-3c493e3c369d">ISearchCrawlScopeManager</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/cfba12eb-4123-4b57-8311-d4fc8f9f514e">The Indexing process</a>



<a href="https://msdn.microsoft.com/7d65d00a-7294-4718-b593-89394b2e416f">Using the Crawl Scope Manager</a>
 

 

