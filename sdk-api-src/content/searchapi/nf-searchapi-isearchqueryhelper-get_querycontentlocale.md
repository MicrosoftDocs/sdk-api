---
UID: NF:searchapi.ISearchQueryHelper.get_QueryContentLocale
title: ISearchQueryHelper::get_QueryContentLocale (searchapi.h)
description: Gets the language code identifier (LCID) for the query.
helpviewer_keywords: ["ISearchQueryHelper interface [search]","get_QueryContentLocale method","ISearchQueryHelper.get_QueryContentLocale","ISearchQueryHelper::get_QueryContentLocale","_search_ISearchQueryHelper_get_QueryContentLocale","get_QueryContentLocale","get_QueryContentLocale method [search]","get_QueryContentLocale method [search]","ISearchQueryHelper interface","search._search_ISearchQueryHelper_get_QueryContentLocale","searchapi/ISearchQueryHelper::get_QueryContentLocale"]
old-location: search\_search_ISearchQueryHelper_get_QueryContentLocale.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\isearchqueryhelper\get_querycontentlocale.htm
ms.date: 12/05/2018
ms.keywords: ISearchQueryHelper interface [search],get_QueryContentLocale method, ISearchQueryHelper.get_QueryContentLocale, ISearchQueryHelper::get_QueryContentLocale, _search_ISearchQueryHelper_get_QueryContentLocale, get_QueryContentLocale, get_QueryContentLocale method [search], get_QueryContentLocale method [search],ISearchQueryHelper interface, search._search_ISearchQueryHelper_get_QueryContentLocale, searchapi/ISearchQueryHelper::get_QueryContentLocale
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
 - ISearchQueryHelper::get_QueryContentLocale
 - searchapi/ISearchQueryHelper::get_QueryContentLocale
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
 - ISearchQueryHelper.get_QueryContentLocale
---

# ISearchQueryHelper::get_QueryContentLocale


## -description

Gets the language code identifier (LCID) for the query.

## -parameters

### -param plcid [out, retval]

Type: <b>LCID*</b>

Receives a pointer to the locale identifier used.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The locale identifier has the components necessary to uniquely identify one of the installed system-defined locales. The locale retrieved is used for word breaking, normalizing, and stemming the string values extracted from the query string. If the locale identifier was not set with <a href="/windows/desktop/api/searchapi/nf-searchapi-isearchqueryhelper-put_querycontentlocale">ISearchQueryHelper::put_QueryContentLocale</a>, the active input locale is retrieved.

Checkout the <a href="/windows/win32/search/-search-sample-dsearch">DSearch code sample</a> to see how to create a class for a static console application to query Windows Search using the Microsoft.Search.Interop assembly for <a href="/windows/desktop/api/searchapi/nn-searchapi-isearchqueryhelper">ISearchQueryHelper</a>.

## -see-also

<a href="/windows/desktop/api/searchapi/nn-searchapi-isearchqueryhelper">ISearchQueryHelper</a>



<a href="/windows/desktop/api/searchapi/nf-searchapi-isearchqueryhelper-put_querycontentlocale">ISearchQueryHelper::put_QueryContentLocale</a>



<a href="/windows/desktop/search/-search-3x-wds-qryidx-overview">Querying the Index Programmatically</a>



<a href="/windows/desktop/search/-search-sql-windowssearch-entry">Querying the Index with Windows Search SQL Syntax</a>