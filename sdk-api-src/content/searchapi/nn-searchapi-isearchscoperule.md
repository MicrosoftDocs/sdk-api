---
UID: NN:searchapi.ISearchScopeRule
title: ISearchScopeRule (searchapi.h)
description: Provides methods to define scope rules for crawling and indexing.
helpviewer_keywords: ["ISearchScopeRule","ISearchScopeRule interface [search]","ISearchScopeRule interface [search]","described","_search_ISearchScopeRule","search._search_ISearchScopeRule","searchapi/ISearchScopeRule"]
old-location: search\_search_ISearchScopeRule.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\crawlscope\isearchscoperule\isearchscoperule.htm
ms.date: 12/05/2018
ms.keywords: ISearchScopeRule, ISearchScopeRule interface [search], ISearchScopeRule interface [search],described, _search_ISearchScopeRule, search._search_ISearchScopeRule, searchapi/ISearchScopeRule
f1_keywords:
- searchapi/ISearchScopeRule
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
- ISearchScopeRule
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
---

# ISearchScopeRule interface


## -description


Provides methods to define scope rules for crawling and indexing.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISearchScopeRule</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISearchScopeRule</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nf-searchapi-isearchscoperule-get_followflags">get_FollowFlags</a>
</td>
<td align="left" width="63%">
Not currently supported.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nf-searchapi-isearchscoperule-get_isdefault">get_IsDefault</a>
</td>
<td align="left" width="63%">
Gets a value that identifies whether this is a default rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nf-searchapi-isearchscoperule-get_isincluded">get_IsIncluded</a>
</td>
<td align="left" width="63%">
Gets a value identifying whether this rule is an inclusion rule. Inclusion rules identify scopes that should be included in the crawl scope.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nf-searchapi-isearchscoperule-get_patternorurl">get_PatternOrURL</a>
</td>
<td align="left" width="63%">
Gets the pattern or URL for the rule. The scope rules determine what URLs or paths to include or exclude. 

</td>
</tr>
</table> 


## -remarks

For a sample that demonstrates how to define command line options for Crawl Scope Manager (CSM) indexing operations, see the [CrawlScopeCommandLine](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/CrawlScopeCommandLine) sample.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/search/-search-3x-wds-extidx-csm">Using the Crawl Scope Manager</a>
 

 

