---
UID: NN:searchapi.ISearchScopeRule
title: ISearchScopeRule
author: windows-sdk-content
description: Provides methods to define scope rules for crawling and indexing.
old-location: search\_search_ISearchScopeRule.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\crawlscope\isearchscoperule\isearchscoperule.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: ISearchScopeRule, ISearchScopeRule interface [search], ISearchScopeRule interface [search],described, _search_ISearchScopeRule, search._search_ISearchScopeRule, searchapi/ISearchScopeRule
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
 - ISearchScopeRule
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
---

# ISearchScopeRule interface


## -description


Provides methods to define scope rules for crawling and indexing.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISearchScopeRule</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ISearchScopeRule</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISearchScopeRule</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7c0730fe-78e3-41bd-8923-13016db06643">get_FollowFlags</a>
</td>
<td align="left" width="63%">
Not currently supported.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ed424c50-c4ca-475d-83b8-038895826548">get_IsDefault</a>
</td>
<td align="left" width="63%">
Gets a value that identifies whether this is a default rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/77a2fc52-6cc8-4cb2-82ab-b21e4590b5a9">get_IsIncluded</a>
</td>
<td align="left" width="63%">
Gets a value identifying whether this rule is an inclusion rule. Inclusion rules identify scopes that should be included in the crawl scope.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/133d300f-7dbf-4ecd-abb5-50491322d1a0">get_PatternOrURL</a>
</td>
<td align="left" width="63%">
Gets the pattern or URL for the rule. The scope rules determine what URLs or paths to include or exclude. 

</td>
</tr>
</table> 


## -remarks



<b>Windows 7 and later</b>: the CrawlScopeCommandLine code sample, available on <a href="http://go.microsoft.com/fwlink/p/?linkid=155654">Code Gallery</a> and the <a href="http://go.microsoft.com/fwlink/p/?linkid=129787">Windows 7 SDK</a>, demonstrates how to define command line options for Crawl Scope Manager (CSM) indexing operations.




## -see-also




<a href="https://msdn.microsoft.com/7d65d00a-7294-4718-b593-89394b2e416f">Using the Crawl Scope Manager</a>
 

 

