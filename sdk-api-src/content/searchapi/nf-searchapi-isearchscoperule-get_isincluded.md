---
UID: NF:searchapi.ISearchScopeRule.get_IsIncluded
title: ISearchScopeRule::get_IsIncluded (searchapi.h)
description: Gets a value identifying whether this rule is an inclusion rule. Inclusion rules identify scopes that should be included in the crawl scope.
helpviewer_keywords: ["ISearchScopeRule interface [search]","get_IsIncluded method","ISearchScopeRule.get_IsIncluded","ISearchScopeRule::get_IsIncluded","_search_ISearchScopeRule_get_IsIncluded","get_IsIncluded","get_IsIncluded method [search]","get_IsIncluded method [search]","ISearchScopeRule interface","search._search_ISearchScopeRule_get_IsIncluded","searchapi/ISearchScopeRule::get_IsIncluded"]
old-location: search\_search_ISearchScopeRule_get_IsIncluded.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\crawlscope\isearchscoperule\get_isincluded.htm
ms.date: 12/05/2018
ms.keywords: ISearchScopeRule interface [search],get_IsIncluded method, ISearchScopeRule.get_IsIncluded, ISearchScopeRule::get_IsIncluded, _search_ISearchScopeRule_get_IsIncluded, get_IsIncluded, get_IsIncluded method [search], get_IsIncluded method [search],ISearchScopeRule interface, search._search_ISearchScopeRule_get_IsIncluded, searchapi/ISearchScopeRule::get_IsIncluded
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
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
f1_keywords:
 - ISearchScopeRule::get_IsIncluded
 - searchapi/ISearchScopeRule::get_IsIncluded
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Searchapi.h
api_name:
 - ISearchScopeRule.get_IsIncluded
---

# ISearchScopeRule::get_IsIncluded


## -description

Gets a value identifying whether this rule is an inclusion rule. Inclusion rules identify scopes that should be included in the crawl scope.

## -parameters

### -param pfIsIncluded [out, retval]

Type: <b>BOOL*</b>

On return, points to <b>TRUE</b> if this rule is an inclusion rule, <b>FALSE</b> otherwise.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

<b>Windows 7 and later</b>: Check out the <a href="/windows/win32/search/-search-sample-crawlscopecommandline">CrawlScopeCommandLine code sample</a> to see how to define command line options for Crawl Scope Manager (CSM) indexing operations.