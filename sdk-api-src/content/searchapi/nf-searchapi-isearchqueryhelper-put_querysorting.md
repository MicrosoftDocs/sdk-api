---
UID: NF:searchapi.ISearchQueryHelper.put_QuerySorting
title: ISearchQueryHelper::put_QuerySorting (searchapi.h)
description: Sets the sort order for the query result set.
old-location: search\_search_ISearchQueryHelper_put_QuerySorting.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\isearchqueryhelper\put_querysorting.htm
ms.date: 12/05/2018
ms.keywords: ISearchQueryHelper interface [search],put_QuerySorting method, ISearchQueryHelper.put_QuerySorting, ISearchQueryHelper::put_QuerySorting, _search_ISearchQueryHelper_put_QuerySorting, put_QuerySorting, put_QuerySorting method [search], put_QuerySorting method [search],ISearchQueryHelper interface, search._search_ISearchQueryHelper_put_QuerySorting, searchapi/ISearchQueryHelper::put_QuerySorting
ms.topic: method
f1_keywords:
- searchapi/ISearchQueryHelper.put_QuerySorting
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
- ISearchQueryHelper.put_QuerySorting
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
---

# ISearchQueryHelper::put_QuerySorting


## -description


Sets the sort order for the query result set.


## -parameters




### -param pszSorting [in]

Type: <b>LPCWSTR</b>

A comma-delimited, null-terminated Unicode string that specifies the sort order.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



<i>ppszSorting</i> must be a valid ORDER BY clause (without the ORDER BY keyword). <a href="https://docs.microsoft.com/windows/desktop/search/-search-sql-ovwofsearchquery">Windows Search SQL</a> supports sorting on multiple properties, in either ascending (ASC) or descending (DESC) order on each property. For example, <i>ppszSorting</i> might contain the following:

<code>System.ItemAuthors ASC, System.ItemDate DESC</code>

The DSearch code sample, available on <a href="http://go.microsoft.com/fwlink/p/?linkid=155654">Code Gallery</a> and the <a href="http://go.microsoft.com/fwlink/p/?linkid=129787">Windows 7 SDK</a>, demonstrates how to create a class for a static console application to query Windows Search using the Microsoft.Search.Interop assembly for <a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nn-searchapi-isearchqueryhelper">ISearchQueryHelper</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nn-searchapi-isearchqueryhelper">ISearchQueryHelper</a>



<a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nf-searchapi-isearchqueryhelper-get_querysorting">ISearchQueryHelper::get_QuerySorting</a>



<a href="https://docs.microsoft.com/windows/desktop/search/-search-3x-wds-qryidx-overview">Querying the Index Programmatically</a>



<a href="https://docs.microsoft.com/windows/desktop/search/-search-sql-windowssearch-entry">Querying the Index with Windows Search SQL Syntax</a>
 

 

