---
UID: NF:searchapi.ISearchQueryHelper.get_QueryWhereRestrictions
title: ISearchQueryHelper::get_QueryWhereRestrictions (searchapi.h)
description: Gets the restrictions appended to a query in WHERE clauses.
helpviewer_keywords: ["ISearchQueryHelper interface [search]","get_QueryWhereRestrictions method","ISearchQueryHelper.get_QueryWhereRestrictions","ISearchQueryHelper::get_QueryWhereRestrictions","_search_ISearchQueryHelper_get_QueryWhereRestrictions","get_QueryWhereRestrictions","get_QueryWhereRestrictions method [search]","get_QueryWhereRestrictions method [search]","ISearchQueryHelper interface","search._search_ISearchQueryHelper_get_QueryWhereRestrictions","searchapi/ISearchQueryHelper::get_QueryWhereRestrictions"]
old-location: search\_search_ISearchQueryHelper_get_QueryWhereRestrictions.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\isearchqueryhelper\get_querywhererestrictions.htm
ms.date: 12/05/2018
ms.keywords: ISearchQueryHelper interface [search],get_QueryWhereRestrictions method, ISearchQueryHelper.get_QueryWhereRestrictions, ISearchQueryHelper::get_QueryWhereRestrictions, _search_ISearchQueryHelper_get_QueryWhereRestrictions, get_QueryWhereRestrictions, get_QueryWhereRestrictions method [search], get_QueryWhereRestrictions method [search],ISearchQueryHelper interface, search._search_ISearchQueryHelper_get_QueryWhereRestrictions, searchapi/ISearchQueryHelper::get_QueryWhereRestrictions
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
 - ISearchQueryHelper::get_QueryWhereRestrictions
 - searchapi/ISearchQueryHelper::get_QueryWhereRestrictions
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
 - ISearchQueryHelper.get_QueryWhereRestrictions
---

# ISearchQueryHelper::get_QueryWhereRestrictions


## -description

Gets the restrictions appended to a query in WHERE clauses.

## -parameters

### -param ppszRestrictions [out, retval]

Type: <b>LPWSTR*</b>

Receives a pointer to a comma-delimited null-terminated Unicode string that specifies one or more restrictions appended to a query by WHERE clauses.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Checkout the <a href="/windows/win32/search/-search-sample-dsearch">DSearch code sample</a> to see how to create a class for a static console application to query Windows Search using the Microsoft.Search.Interop assembly for <a href="/windows/desktop/api/searchapi/nn-searchapi-isearchqueryhelper">ISearchQueryHelper</a>.

## -see-also

<a href="/windows/desktop/api/searchapi/nn-searchapi-isearchqueryhelper">ISearchQueryHelper</a>



<a href="/windows/desktop/api/searchapi/nf-searchapi-isearchqueryhelper-put_querywhererestrictions">ISearchQueryHelper::put_QueryWhereRestrictions</a>



<a href="/windows/desktop/search/-search-3x-wds-qryidx-overview">Querying the Index Programmatically</a>



<a href="/windows/desktop/search/-search-sql-windowssearch-entry">Querying the Index with Windows Search SQL Syntax</a>