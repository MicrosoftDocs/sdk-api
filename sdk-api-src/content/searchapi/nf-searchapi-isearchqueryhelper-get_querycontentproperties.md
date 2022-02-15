---
UID: NF:searchapi.ISearchQueryHelper.get_QueryContentProperties
title: ISearchQueryHelper::get_QueryContentProperties (searchapi.h)
description: Gets the list of properties included in the query when search terms do not explicitly specify a property.
helpviewer_keywords: ["ISearchQueryHelper interface [search]","get_QueryContentProperties method","ISearchQueryHelper.get_QueryContentProperties","ISearchQueryHelper::get_QueryContentProperties","_search_ISearchQueryHelper_get_QueryContentProperties","get_QueryContentProperties","get_QueryContentProperties method [search]","get_QueryContentProperties method [search]","ISearchQueryHelper interface","search._search_ISearchQueryHelper_get_QueryContentProperties","searchapi/ISearchQueryHelper::get_QueryContentProperties"]
old-location: search\_search_ISearchQueryHelper_get_QueryContentProperties.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\isearchqueryhelper\get_querycontentproperties.htm
ms.date: 12/05/2018
ms.keywords: ISearchQueryHelper interface [search],get_QueryContentProperties method, ISearchQueryHelper.get_QueryContentProperties, ISearchQueryHelper::get_QueryContentProperties, _search_ISearchQueryHelper_get_QueryContentProperties, get_QueryContentProperties, get_QueryContentProperties method [search], get_QueryContentProperties method [search],ISearchQueryHelper interface, search._search_ISearchQueryHelper_get_QueryContentProperties, searchapi/ISearchQueryHelper::get_QueryContentProperties
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
 - ISearchQueryHelper::get_QueryContentProperties
 - searchapi/ISearchQueryHelper::get_QueryContentProperties
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
 - ISearchQueryHelper.get_QueryContentProperties
---

# ISearchQueryHelper::get_QueryContentProperties


## -description

Gets the list of properties included in the query when search terms do not explicitly specify a property.

## -parameters

### -param ppszContentProperties [out, retval]

Type: <b>LPWSTR*</b>

Receives a pointer to a comma-delimited, null-terminated Unicode string of content properties to search. If <i>ppszContentProperties</i> is <b>NULL</b>,  all properties are searched.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Search terms may or may not be explicitly prefixed by a property ("author:Irina" or just "Irina"). If <i>SEARCH_ADVANCED_QUERY_SYNTAX</i> or <i>NO_QUERY_SYNTAX</i> is set in <a href="/windows/desktop/api/searchapi/nf-searchapi-isearchqueryhelper-put_querysyntax">ISearchQueryHelper::put_QuerySyntax</a>, all search terms not prefixed by a property keyword are matched against the list of properties in <i>ppszContentProperties</i>.

Checkout the <a href="/windows/win32/search/-search-sample-dsearch">DSearch code sample</a> to see how to create a class for a static console application to query Windows Search using the Microsoft.Search.Interop assembly for <a href="/windows/desktop/api/searchapi/nn-searchapi-isearchqueryhelper">ISearchQueryHelper</a>.

## -see-also

<a href="/windows/desktop/api/searchapi/nn-searchapi-isearchqueryhelper">ISearchQueryHelper</a>



<a href="/windows/desktop/api/searchapi/nf-searchapi-isearchqueryhelper-put_querycontentproperties">ISearchQueryHelper::put_QueryContentProperties</a>



<a href="/windows/desktop/search/-search-3x-wds-qryidx-overview">Querying the Index Programmatically</a>



<a href="/windows/desktop/search/-search-sql-windowssearch-entry">Querying the Index with Windows Search SQL Syntax</a>



<a href="https://msdn.microsoft.com/library/ff518152(v=VS.85).aspx">System Properties</a>