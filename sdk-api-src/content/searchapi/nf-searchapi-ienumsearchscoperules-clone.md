---
UID: NF:searchapi.IEnumSearchScopeRules.Clone
title: IEnumSearchScopeRules::Clone (searchapi.h)
description: Creates a copy of this IEnumSearchScopeRules object with the same contents and state as the current one.
helpviewer_keywords: ["Clone","Clone method [search]","Clone method [search]","IEnumSearchScopeRules interface","IEnumSearchScopeRules interface [search]","Clone method","IEnumSearchScopeRules.Clone","IEnumSearchScopeRules::Clone","_search_IEnumSearchScopeRules_Clone","search._search_IEnumSearchScopeRules_Clone","searchapi/IEnumSearchScopeRules::Clone"]
old-location: search\_search_IEnumSearchScopeRules_Clone.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\crawlscope\ienumsearchscoperules\clone.htm
ms.date: 12/05/2018
ms.keywords: Clone, Clone method [search], Clone method [search],IEnumSearchScopeRules interface, IEnumSearchScopeRules interface [search],Clone method, IEnumSearchScopeRules.Clone, IEnumSearchScopeRules::Clone, _search_IEnumSearchScopeRules_Clone, search._search_IEnumSearchScopeRules_Clone, searchapi/IEnumSearchScopeRules::Clone
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IEnumSearchScopeRules::Clone
 - searchapi/IEnumSearchScopeRules::Clone
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
 - IEnumSearchScopeRules.Clone
---

# IEnumSearchScopeRules::Clone


## -description

Creates a copy of this <a href="/windows/desktop/api/searchapi/nn-searchapi-ienumsearchscoperules">IEnumSearchScopeRules</a> object with the same contents and state as the current one.

## -parameters

### -param ppenum [out, retval]

Type: <b><a href="/windows/desktop/api/searchapi/nn-searchapi-ienumsearchscoperules">IEnumSearchScopeRules</a>**</b>

On return, contains a pointer to the cloned <a href="/windows/desktop/api/searchapi/nn-searchapi-ienumsearchscoperules">IEnumSearchScopeRules</a> object. The calling application must free the new object by calling its <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> method.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

<b>Windows 7 and later</b>: Check out the <a href="/windows/win32/search/-search-sample-crawlscopecommandline">CrawlScopeCommandLine code sample</a> to see how to define command line options for Crawl Scope Manager (CSM) indexing operations.