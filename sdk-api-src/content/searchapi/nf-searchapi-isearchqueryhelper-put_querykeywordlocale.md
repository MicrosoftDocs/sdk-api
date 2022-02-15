---
UID: NF:searchapi.ISearchQueryHelper.put_QueryKeywordLocale
title: ISearchQueryHelper::put_QueryKeywordLocale (searchapi.h)
description: Sets the language code identifier (LCID) for the locale to use when parsing Advanced Query Syntax (AQS) keywords.
helpviewer_keywords: ["ISearchQueryHelper interface [search]","put_QueryKeywordLocale method","ISearchQueryHelper.put_QueryKeywordLocale","ISearchQueryHelper::put_QueryKeywordLocale","_search_ISearchQueryHelper_put_QueryKeywordLocale","put_QueryKeywordLocale","put_QueryKeywordLocale method [search]","put_QueryKeywordLocale method [search]","ISearchQueryHelper interface","search._search_ISearchQueryHelper_put_QueryKeywordLocale","searchapi/ISearchQueryHelper::put_QueryKeywordLocale"]
old-location: search\_search_ISearchQueryHelper_put_QueryKeywordLocale.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\isearchqueryhelper\put_querykeywordlocale.htm
ms.date: 12/05/2018
ms.keywords: ISearchQueryHelper interface [search],put_QueryKeywordLocale method, ISearchQueryHelper.put_QueryKeywordLocale, ISearchQueryHelper::put_QueryKeywordLocale, _search_ISearchQueryHelper_put_QueryKeywordLocale, put_QueryKeywordLocale, put_QueryKeywordLocale method [search], put_QueryKeywordLocale method [search],ISearchQueryHelper interface, search._search_ISearchQueryHelper_put_QueryKeywordLocale, searchapi/ISearchQueryHelper::put_QueryKeywordLocale
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
 - ISearchQueryHelper::put_QueryKeywordLocale
 - searchapi/ISearchQueryHelper::put_QueryKeywordLocale
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
 - ISearchQueryHelper.put_QueryKeywordLocale
---

# ISearchQueryHelper::put_QueryKeywordLocale


## -description

Sets the language code identifier (LCID) for the locale to use when parsing Advanced Query Syntax (AQS) keywords.

## -parameters

### -param lcid [in]

Type: <b>LCID</b>

Sets the LCID for the locale to use when parsing Advanced Query Syntax (AQS) keywords.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Checkout the <a href="/windows/win32/search/-search-sample-dsearch">DSearch code sample</a> to see how to create a class for a static console application to query Windows Search using the Microsoft.Search.Interop assembly for <a href="/windows/desktop/api/searchapi/nn-searchapi-isearchqueryhelper">ISearchQueryHelper</a>.

## -see-also

<a href="/windows/desktop/api/searchapi/nn-searchapi-isearchqueryhelper">ISearchQueryHelper</a>



<a href="/windows/desktop/api/searchapi/nf-searchapi-isearchqueryhelper-get_querykeywordlocale">ISearchQueryHelper::get_QueryKeywordLocale</a>



<a href="/windows/desktop/search/-search-3x-wds-qryidx-overview">Querying the Index Programmatically</a>



<a href="/windows/desktop/search/-search-sql-windowssearch-entry">Querying the Index with Windows Search SQL Syntax</a>