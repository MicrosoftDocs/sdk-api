---
UID: NF:searchapi.ISearchQueryHelper.put_QueryMaxResults
title: ISearchQueryHelper::put_QueryMaxResults (searchapi.h)
description: Sets the maximum number of results to be returned by a query.
helpviewer_keywords: ["ISearchQueryHelper interface [search]","put_QueryMaxResults method","ISearchQueryHelper.put_QueryMaxResults","ISearchQueryHelper::put_QueryMaxResults","_search_ISearchQueryHelper_put_QueryMaxResults","put_QueryMaxResults","put_QueryMaxResults method [search]","put_QueryMaxResults method [search]","ISearchQueryHelper interface","search._search_ISearchQueryHelper_put_QueryMaxResults","searchapi/ISearchQueryHelper::put_QueryMaxResults"]
old-location: search\_search_ISearchQueryHelper_put_QueryMaxResults.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\isearchqueryhelper\put_querymaxresults.htm
ms.date: 12/05/2018
ms.keywords: ISearchQueryHelper interface [search],put_QueryMaxResults method, ISearchQueryHelper.put_QueryMaxResults, ISearchQueryHelper::put_QueryMaxResults, _search_ISearchQueryHelper_put_QueryMaxResults, put_QueryMaxResults, put_QueryMaxResults method [search], put_QueryMaxResults method [search],ISearchQueryHelper interface, search._search_ISearchQueryHelper_put_QueryMaxResults, searchapi/ISearchQueryHelper::put_QueryMaxResults
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
 - ISearchQueryHelper::put_QueryMaxResults
 - searchapi/ISearchQueryHelper::put_QueryMaxResults
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
 - ISearchQueryHelper.put_QueryMaxResults
---

# ISearchQueryHelper::put_QueryMaxResults


## -description

Sets the maximum number of results to be returned by a query.

## -parameters

### -param cMaxResults [in]

Type: <b>LONG</b>

The maximum number of results to be returned. Negative numbers return all results.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Checkout the <a href="/windows/win32/search/-search-sample-dsearch">DSearch code sample</a> to see how to create a class for a static console application to query Windows Search using the Microsoft.Search.Interop assembly for <a href="/windows/desktop/api/searchapi/nn-searchapi-isearchqueryhelper">ISearchQueryHelper</a>.

## -see-also

<a href="/windows/desktop/api/searchapi/nn-searchapi-isearchqueryhelper">ISearchQueryHelper</a>



<a href="/windows/desktop/api/searchapi/nf-searchapi-isearchqueryhelper-get_querymaxresults">ISearchQueryHelper::get_QueryMaxResults</a>



<a href="/windows/desktop/search/-search-3x-wds-qryidx-overview">Querying the Index Programmatically</a>



<a href="/windows/desktop/search/-search-sql-windowssearch-entry">Querying the Index with Windows Search SQL Syntax</a>