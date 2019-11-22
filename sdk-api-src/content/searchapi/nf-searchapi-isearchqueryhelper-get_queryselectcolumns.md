---
UID: NF:searchapi.ISearchQueryHelper.get_QuerySelectColumns
title: ISearchQueryHelper::get_QuerySelectColumns (searchapi.h)

description: Gets the columns (or properties) requested in the SELECT statement of the query.
old-location: search\_search_ISearchQueryHelper_get_QuerySelectColumns.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\isearchqueryhelper\get_queryselectcolumns.htm

ms.date: 12/05/2018
ms.keywords: ISearchQueryHelper interface [search],get_QuerySelectColumns method, ISearchQueryHelper.get_QuerySelectColumns, ISearchQueryHelper::get_QuerySelectColumns, _search_ISearchQueryHelper_get_QuerySelectColumns, get_QuerySelectColumns, get_QuerySelectColumns method [search], get_QuerySelectColumns method [search],ISearchQueryHelper interface, search._search_ISearchQueryHelper_get_QuerySelectColumns, searchapi/ISearchQueryHelper::get_QuerySelectColumns
ms.topic: method
f1_keywords: 
 - "searchapi/ISearchQueryHelper.get_QuerySelectColumns"
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
 - ISearchQueryHelper.get_QuerySelectColumns
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
---

# ISearchQueryHelper::get_QuerySelectColumns


## -description


Gets the columns (or properties) requested in the SELECT statement of the query.


## -parameters




### -param ppszSelectColumns [out, retval]

Type: <b>LPWSTR*</b>

Receives a pointer to a comma-delimited, null-terminated Unicode string that specifies the columns (or properties) to be returned from a query.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Items are represented in the property store as a row. Each row contains a number of columns that represent properties for that row or object. Not all items will have a value for a particular property. Properties must be in the property store to be subject to a select operation.

The DSearch code sample, available on <a href="http://go.microsoft.com/fwlink/p/?linkid=155654">Code Gallery</a> and the <a href="http://go.microsoft.com/fwlink/p/?linkid=129787">Windows 7 SDK</a>, demonstrates how to create a class for a static console application to query Windows Search using the Microsoft.Search.Interop assembly for <a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nn-searchapi-isearchqueryhelper">ISearchQueryHelper</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nn-searchapi-isearchqueryhelper">ISearchQueryHelper</a>



<a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nf-searchapi-isearchqueryhelper-put_queryselectcolumns">ISearchQueryHelper::put_QuerySelectColumns</a>



<a href="https://docs.microsoft.com/windows/desktop/search/-search-3x-wds-qryidx-overview">Querying the Index Programmatically</a>



<a href="https://docs.microsoft.com/windows/desktop/search/-search-sql-windowssearch-entry">Querying the Index with Windows Search SQL Syntax</a>



<a href="https://msdn.microsoft.com/library/ff518152(v=VS.85).aspx">System Properties</a>
 

 

