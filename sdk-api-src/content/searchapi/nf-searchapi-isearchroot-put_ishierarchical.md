---
UID: NF:searchapi.ISearchRoot.put_IsHierarchical
title: ISearchRoot::put_IsHierarchical (searchapi.h)
description: Sets a value that indicates whether the search is rooted on a hierarchical tree structure.
helpviewer_keywords: ["ISearchRoot interface [search]","put_IsHierarchical method","ISearchRoot.put_IsHierarchical","ISearchRoot::put_IsHierarchical","_search_ISearchRoot_put_IsHierarchical","put_IsHierarchical","put_IsHierarchical method [search]","put_IsHierarchical method [search]","ISearchRoot interface","search._search_ISearchRoot_put_IsHierarchical","searchapi/ISearchRoot::put_IsHierarchical"]
old-location: search\_search_ISearchRoot_put_IsHierarchical.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\crawlscope\isearchroot\put_ishierarchical.htm
ms.date: 12/05/2018
ms.keywords: ISearchRoot interface [search],put_IsHierarchical method, ISearchRoot.put_IsHierarchical, ISearchRoot::put_IsHierarchical, _search_ISearchRoot_put_IsHierarchical, put_IsHierarchical, put_IsHierarchical method [search], put_IsHierarchical method [search],ISearchRoot interface, search._search_ISearchRoot_put_IsHierarchical, searchapi/ISearchRoot::put_IsHierarchical
req.header: searchapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISearchRoot::put_IsHierarchical
 - searchapi/ISearchRoot::put_IsHierarchical
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
 - ISearchRoot.put_IsHierarchical
---

# ISearchRoot::put_IsHierarchical


## -description

Sets a value that indicates whether the search is rooted on a hierarchical tree structure.

## -parameters

### -param fIsHierarchical [in]

Type: <b>BOOL</b>

<b>TRUE</b> for hierarchical tree structures, <b>FALSE</b> for non-hierarchical systems such as websites.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

<b>Windows 7 and later</b>: Check out the <a href="/windows/win32/search/-search-sample-crawlscopecommandline">CrawlScopeCommandLine code sample</a> to see how to define command line 
options for Crawl Scope Manager (CSM) indexing operations.