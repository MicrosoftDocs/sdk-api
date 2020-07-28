---
UID: NF:searchapi.ISearchQueryHelper.get_QueryKeywordLocale
title: ISearchQueryHelper::get_QueryKeywordLocale (searchapi.h)
description: Gets the language code identifier (LCID) for the locale to use when parsing Advanced Query Syntax (AQS) keywords.
helpviewer_keywords: ["ISearchQueryHelper interface [search]","get_QueryKeywordLocale method","ISearchQueryHelper.get_QueryKeywordLocale","ISearchQueryHelper::get_QueryKeywordLocale","_search_ISearchQueryHelper_get_QueryKeywordLocale","get_QueryKeywordLocale","get_QueryKeywordLocale method [search]","get_QueryKeywordLocale method [search]","ISearchQueryHelper interface","search._search_ISearchQueryHelper_get_QueryKeywordLocale","searchapi/ISearchQueryHelper::get_QueryKeywordLocale"]
old-location: search\_search_ISearchQueryHelper_get_QueryKeywordLocale.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\isearchqueryhelper\get_querykeywordlocale.htm
ms.date: 12/05/2018
ms.keywords: ISearchQueryHelper interface [search],get_QueryKeywordLocale method, ISearchQueryHelper.get_QueryKeywordLocale, ISearchQueryHelper::get_QueryKeywordLocale, _search_ISearchQueryHelper_get_QueryKeywordLocale, get_QueryKeywordLocale, get_QueryKeywordLocale method [search], get_QueryKeywordLocale method [search],ISearchQueryHelper interface, search._search_ISearchQueryHelper_get_QueryKeywordLocale, searchapi/ISearchQueryHelper::get_QueryKeywordLocale
f1_keywords:
- searchapi/ISearchQueryHelper.get_QueryKeywordLocale
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Searchapi.h
api_name:
- ISearchQueryHelper.get_QueryKeywordLocale
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
---

# ISearchQueryHelper::get_QueryKeywordLocale


## -description


Gets the language code identifier (LCID) for the locale to use when parsing Advanced Query Syntax (AQS) keywords.


## -parameters




### -param plcid [out, retval]

Type: <b>LCID*</b>

Receives a pointer to the LCID for the locale to use when parsing Advanced Query Syntax (AQS) keywords.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks

Checkout the <a href="https://docs.microsoft.com/windows/win32/search/-search-sample-dsearch">DSearch code sample</a> to see how to create a class for a static console application to query Windows Search using the Microsoft.Search.Interop assembly for <a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nn-searchapi-isearchqueryhelper">ISearchQueryHelper</a>.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nn-searchapi-isearchqueryhelper">ISearchQueryHelper</a>



<a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nf-searchapi-isearchqueryhelper-put_querykeywordlocale">ISearchQueryHelper::put_QueryKeywordLocale</a>



<a href="https://docs.microsoft.com/windows/desktop/search/-search-3x-wds-qryidx-overview">Querying the Index Programmatically</a>



<a href="https://docs.microsoft.com/windows/desktop/search/-search-sql-windowssearch-entry">Querying the Index with Windows Search SQL Syntax</a>
 

 

