---
UID: NF:searchapi.ISearchQueryHelper.put_QueryTermExpansion
title: ISearchQueryHelper::put_QueryTermExpansion (searchapi.h)
description: Sets a value that specifies how query terms are to be expanded.
helpviewer_keywords: ["ISearchQueryHelper interface [search]","put_QueryTermExpansion method","ISearchQueryHelper.put_QueryTermExpansion","ISearchQueryHelper::put_QueryTermExpansion","_search_ISearchQueryHelper_put_QueryTermExpansion","put_QueryTermExpansion","put_QueryTermExpansion method [search]","put_QueryTermExpansion method [search]","ISearchQueryHelper interface","search._search_ISearchQueryHelper_put_QueryTermExpansion","searchapi/ISearchQueryHelper::put_QueryTermExpansion"]
old-location: search\_search_ISearchQueryHelper_put_QueryTermExpansion.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\isearchqueryhelper\put_querytermexpansion.htm
ms.date: 12/05/2018
ms.keywords: ISearchQueryHelper interface [search],put_QueryTermExpansion method, ISearchQueryHelper.put_QueryTermExpansion, ISearchQueryHelper::put_QueryTermExpansion, _search_ISearchQueryHelper_put_QueryTermExpansion, put_QueryTermExpansion, put_QueryTermExpansion method [search], put_QueryTermExpansion method [search],ISearchQueryHelper interface, search._search_ISearchQueryHelper_put_QueryTermExpansion, searchapi/ISearchQueryHelper::put_QueryTermExpansion
req.header: searchapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Searchquery.idl
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
 - ISearchQueryHelper::put_QueryTermExpansion
 - searchapi/ISearchQueryHelper::put_QueryTermExpansion
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
 - ISearchQueryHelper.put_QueryTermExpansion
---

# ISearchQueryHelper::put_QueryTermExpansion


## -description

Sets a value that specifies how query terms are to be expanded.

## -parameters

### -param expandTerms [in]

Type: <b><a href="/windows/desktop/api/searchapi/ne-searchapi-search_term_expansion">SEARCH_TERM_EXPANSION</a></b>

Value from the <a href="/windows/desktop/api/searchapi/ne-searchapi-search_term_expansion">SEARCH_TERM_EXPANSION</a> enumeration that specifies the search term expansion. If not set, the default value is SEARCH_TERM_PREFIX_ALL.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The <b>ISearchQueryHelper::put_QueryTermExpansion</b> method allows for expansion of some query terms with wildcard characters, similar to regular expression expansion. 

While the <a href="/windows/desktop/api/searchapi/ne-searchapi-search_term_expansion">SEARCH_TERM_EXPANSION</a> enumerated type lets you specify stem expansion, Windows Search does not currently support its use with the <a href="/windows/desktop/api/searchapi/nn-searchapi-isearchqueryhelper">ISearchQueryHelper</a> interface.

Checkout the <a href="/windows/win32/search/-search-sample-dsearch">DSearch code sample</a> to see how to create a class for a static console application to query Windows Search using the Microsoft.Search.Interop assembly for <a href="/windows/desktop/api/searchapi/nn-searchapi-isearchqueryhelper">ISearchQueryHelper</a>.

## -see-also

<a href="/windows/desktop/api/searchapi/nn-searchapi-isearchqueryhelper">ISearchQueryHelper</a>



<a href="/windows/desktop/api/searchapi/nf-searchapi-isearchqueryhelper-get_querytermexpansion">ISearchQueryHelper::get_QueryTermExpansion</a>



<a href="/windows/desktop/search/-search-3x-wds-qryidx-overview">Querying the Index Programmatically</a>



<a href="/windows/desktop/search/-search-sql-windowssearch-entry">Querying the Index with Windows Search SQL Syntax</a>



<a href="/windows/desktop/api/searchapi/ne-searchapi-search_term_expansion">SEARCH_TERM_EXPANSION</a>