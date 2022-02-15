---
UID: NF:searchapi.ISearchQueryHelper.put_QueryContentLocale
title: ISearchQueryHelper::put_QueryContentLocale (searchapi.h)
description: Sets the language code identifier (LCID) of the query.
helpviewer_keywords: ["ISearchQueryHelper interface [search]","put_QueryContentLocale method","ISearchQueryHelper.put_QueryContentLocale","ISearchQueryHelper::put_QueryContentLocale","_search_ISearchQueryHelper_put_QueryContentLocale","put_QueryContentLocale","put_QueryContentLocale method [search]","put_QueryContentLocale method [search]","ISearchQueryHelper interface","search._search_ISearchQueryHelper_put_QueryContentLocale","searchapi/ISearchQueryHelper::put_QueryContentLocale"]
old-location: search\_search_ISearchQueryHelper_put_QueryContentLocale.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\isearchqueryhelper\put_querycontentlocale.htm
ms.date: 12/05/2018
ms.keywords: ISearchQueryHelper interface [search],put_QueryContentLocale method, ISearchQueryHelper.put_QueryContentLocale, ISearchQueryHelper::put_QueryContentLocale, _search_ISearchQueryHelper_put_QueryContentLocale, put_QueryContentLocale, put_QueryContentLocale method [search], put_QueryContentLocale method [search],ISearchQueryHelper interface, search._search_ISearchQueryHelper_put_QueryContentLocale, searchapi/ISearchQueryHelper::put_QueryContentLocale
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
 - ISearchQueryHelper::put_QueryContentLocale
 - searchapi/ISearchQueryHelper::put_QueryContentLocale
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
 - ISearchQueryHelper.put_QueryContentLocale
---

# ISearchQueryHelper::put_QueryContentLocale


## -description

Sets the language code identifier (LCID) of the query.

## -parameters

### -param lcid [in]

Type: <b>LCID</b>

Sets the LCID of the query.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The locale identifier has the components necessary to uniquely identify one of the installed system-defined locales. The LCID controls a number of settings including numeric format, date format, currency format, uppercase and lowercase mapping, dictionary sort ordering, tokenization, and others. Although these settings help Windows operating system and Windows Search API provide excellent localized support, unexpected results can occur when documents from one locale are searched by a system set for another locale.

When the <a href="/windows/desktop/api/filter/nn-filter-ifilter">IFilter</a> object processes a document's text properties and content, it reports the language of that document to the content indexer. Using this information, the Search API can apply the appropriate word breaker and noise-words list.

The locale is used for word breaking, normalizing, and stemming the string values that are extracted from the query string. If this method is not used (so the content locale is not set), <a href="/windows/desktop/api/searchapi/nf-searchapi-isearchqueryhelper-get_querycontentlocale">ISearchQueryHelper::get_QueryContentLocale</a> returns the active input locale.

Checkout the <a href="/windows/win32/search/-search-sample-dsearch">DSearch code sample</a> to see how to create a class for a static console application to query Windows Search using the Microsoft.Search.Interop assembly for <a href="/windows/desktop/api/searchapi/nn-searchapi-isearchqueryhelper">ISearchQueryHelper</a>.

## -see-also

<a href="/windows/desktop/api/searchapi/nn-searchapi-isearchqueryhelper">ISearchQueryHelper</a>



<a href="/windows/desktop/api/searchapi/nf-searchapi-isearchqueryhelper-get_querycontentlocale">ISearchQueryHelper::get_QueryContentLocale</a>



<a href="/windows/desktop/search/-search-3x-wds-qryidx-overview">Querying the Index Programmatically</a>



<a href="/windows/desktop/search/-search-sql-windowssearch-entry">Querying the Index with Windows Search SQL Syntax</a>