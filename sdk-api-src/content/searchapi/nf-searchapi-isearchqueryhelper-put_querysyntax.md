---
UID: NF:searchapi.ISearchQueryHelper.put_QuerySyntax
title: ISearchQueryHelper::put_QuerySyntax (searchapi.h)
description: Sets the syntax of the query.
helpviewer_keywords: ["ISearchQueryHelper interface [search]","put_QuerySyntax method","ISearchQueryHelper.put_QuerySyntax","ISearchQueryHelper::put_QuerySyntax","_search_ISearchQueryHelper_put_QuerySyntax","put_QuerySyntax","put_QuerySyntax method [search]","put_QuerySyntax method [search]","ISearchQueryHelper interface","search._search_ISearchQueryHelper_put_QuerySyntax","searchapi/ISearchQueryHelper::put_QuerySyntax"]
old-location: search\_search_ISearchQueryHelper_put_QuerySyntax.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\isearchqueryhelper\put_querysyntax.htm
ms.date: 12/05/2018
ms.keywords: ISearchQueryHelper interface [search],put_QuerySyntax method, ISearchQueryHelper.put_QuerySyntax, ISearchQueryHelper::put_QuerySyntax, _search_ISearchQueryHelper_put_QuerySyntax, put_QuerySyntax, put_QuerySyntax method [search], put_QuerySyntax method [search],ISearchQueryHelper interface, search._search_ISearchQueryHelper_put_QuerySyntax, searchapi/ISearchQueryHelper::put_QuerySyntax
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
 - ISearchQueryHelper::put_QuerySyntax
 - searchapi/ISearchQueryHelper::put_QuerySyntax
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
 - ISearchQueryHelper.put_QuerySyntax
---

# ISearchQueryHelper::put_QuerySyntax


## -description

Sets the syntax of the query.

## -parameters

### -param querySyntax [in]

Type: <b><a href="/windows/desktop/api/searchapi/ne-searchapi-search_query_syntax">SEARCH_QUERY_SYNTAX</a></b>

Flag that specifies the search query syntax. For a list of possible values, see the description of the <a href="/windows/desktop/api/searchapi/ne-searchapi-search_query_syntax">SEARCH_QUERY_SYNTAX</a> enumerated type.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The allowed syntaxes are Simple, Natural Query Syntax (NQS), and Advanced Query Syntax (AQS). If not set, the default query syntax is SEARCH_ADVANCED_QUERY_SYNTAX.

Checkout the <a href="/windows/win32/search/-search-sample-dsearch">DSearch code sample</a> to see how to create a class for a static console application to query Windows Search using the Microsoft.Search.Interop assembly for <a href="/windows/desktop/api/searchapi/nn-searchapi-isearchqueryhelper">ISearchQueryHelper</a>.

## -see-also

<a href="/windows/desktop/api/searchapi/nn-searchapi-isearchqueryhelper">ISearchQueryHelper</a>



<a href="/windows/desktop/api/searchapi/nf-searchapi-isearchqueryhelper-get_querysyntax">ISearchQueryHelper::get_QuerySyntax</a>



<a href="/windows/desktop/search/-search-3x-wds-qryidx-overview">Querying the Index Programmatically</a>



<a href="/windows/desktop/search/-search-sql-windowssearch-entry">Querying the Index with Windows Search SQL Syntax</a>



<a href="/windows/desktop/api/searchapi/ne-searchapi-search_query_syntax">SEARCH_QUERY_SYNTAX</a>