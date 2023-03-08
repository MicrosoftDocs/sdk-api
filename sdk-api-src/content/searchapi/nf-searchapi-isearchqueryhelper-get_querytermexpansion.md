---
UID: NF:searchapi.ISearchQueryHelper.get_QueryTermExpansion
title: ISearchQueryHelper::get_QueryTermExpansion (searchapi.h)
description: Gets the value that specifies how query terms are to be expanded.
helpviewer_keywords: ["ISearchQueryHelper interface [search]","get_QueryTermExpansion method","ISearchQueryHelper.get_QueryTermExpansion","ISearchQueryHelper::get_QueryTermExpansion","_search_ISearchQueryHelper_get_QueryTermExpansion","get_QueryTermExpansion","get_QueryTermExpansion method [search]","get_QueryTermExpansion method [search]","ISearchQueryHelper interface","search._search_ISearchQueryHelper_get_QueryTermExpansion","searchapi/ISearchQueryHelper::get_QueryTermExpansion"]
old-location: search\_search_ISearchQueryHelper_get_QueryTermExpansion.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\isearchqueryhelper\get_querytermexpansion.htm
ms.date: 12/05/2018
ms.keywords: ISearchQueryHelper interface [search],get_QueryTermExpansion method, ISearchQueryHelper.get_QueryTermExpansion, ISearchQueryHelper::get_QueryTermExpansion, _search_ISearchQueryHelper_get_QueryTermExpansion, get_QueryTermExpansion, get_QueryTermExpansion method [search], get_QueryTermExpansion method [search],ISearchQueryHelper interface, search._search_ISearchQueryHelper_get_QueryTermExpansion, searchapi/ISearchQueryHelper::get_QueryTermExpansion
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
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
f1_keywords:
 - ISearchQueryHelper::get_QueryTermExpansion
 - searchapi/ISearchQueryHelper::get_QueryTermExpansion
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
 - ISearchQueryHelper.get_QueryTermExpansion
---

# ISearchQueryHelper::get_QueryTermExpansion


## -description

Gets the value that specifies how query terms are to be expanded.

## -parameters

### -param pExpandTerms [out, retval]

Type: <b><a href="/windows/desktop/api/searchapi/ne-searchapi-search_term_expansion">SEARCH_TERM_EXPANSION</a>*</b>

Receives a pointer to a value from the <a href="/windows/desktop/api/searchapi/ne-searchapi-search_term_expansion">SEARCH_TERM_EXPANSION</a> enumeration that specifies the query term expansion.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

While the <a href="/windows/desktop/api/searchapi/ne-searchapi-search_term_expansion">SEARCH_TERM_EXPANSION</a> enumerated type lets you specify stem expansion, Windows Search does not currently support its use with the <a href="/windows/desktop/api/searchapi/nn-searchapi-isearchqueryhelper">ISearchQueryHelper</a> interface.

Checkout the <a href="/windows/win32/search/-search-sample-dsearch">DSearch code sample</a> to see how to create a class for a static console application to query Windows Search using the Microsoft.Search.Interop assembly for <a href="/windows/desktop/api/searchapi/nn-searchapi-isearchqueryhelper">ISearchQueryHelper</a>.

## -see-also

<a href="/windows/desktop/api/searchapi/nn-searchapi-isearchqueryhelper">ISearchQueryHelper</a>



<a href="/windows/desktop/api/searchapi/nf-searchapi-isearchqueryhelper-put_querytermexpansion">ISearchQueryHelper::put_QueryTermExpansion</a>



<a href="/windows/desktop/search/-search-3x-wds-qryidx-overview">Querying the Index Programmatically</a>



<a href="/windows/desktop/search/-search-sql-windowssearch-entry">Querying the Index with Windows Search SQL Syntax</a>



<a href="/windows/desktop/api/searchapi/ne-searchapi-search_term_expansion">SEARCH_TERM_EXPANSION</a>