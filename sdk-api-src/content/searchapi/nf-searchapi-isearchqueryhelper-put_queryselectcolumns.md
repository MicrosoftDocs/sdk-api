---
UID: NF:searchapi.ISearchQueryHelper.put_QuerySelectColumns
title: ISearchQueryHelper::put_QuerySelectColumns (searchapi.h)
description: Sets the columns (or properties) requested in the select statement.
helpviewer_keywords: ["ISearchQueryHelper interface [search]","put_QuerySelectColumns method","ISearchQueryHelper.put_QuerySelectColumns","ISearchQueryHelper::put_QuerySelectColumns","_search_ISearchQueryHelper_put_QuerySelectColumns","put_QuerySelectColumns","put_QuerySelectColumns method [search]","put_QuerySelectColumns method [search]","ISearchQueryHelper interface","search._search_ISearchQueryHelper_put_QuerySelectColumns","searchapi/ISearchQueryHelper::put_QuerySelectColumns"]
old-location: search\_search_ISearchQueryHelper_put_QuerySelectColumns.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\isearchqueryhelper\put_queryselectcolumns.htm
ms.date: 12/05/2018
ms.keywords: ISearchQueryHelper interface [search],put_QuerySelectColumns method, ISearchQueryHelper.put_QuerySelectColumns, ISearchQueryHelper::put_QuerySelectColumns, _search_ISearchQueryHelper_put_QuerySelectColumns, put_QuerySelectColumns, put_QuerySelectColumns method [search], put_QuerySelectColumns method [search],ISearchQueryHelper interface, search._search_ISearchQueryHelper_put_QuerySelectColumns, searchapi/ISearchQueryHelper::put_QuerySelectColumns
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
 - ISearchQueryHelper::put_QuerySelectColumns
 - searchapi/ISearchQueryHelper::put_QuerySelectColumns
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
 - ISearchQueryHelper.put_QuerySelectColumns
---

# ISearchQueryHelper::put_QuerySelectColumns


## -description

Sets the columns (or properties) requested in the select statement.

## -parameters

### -param pszSelectColumns [in]

Type: <b>LPCWSTR</b>

Pointer to a comma-delimited, null-terminated Unicode string that specifies one or more columns in the property store. Separate multiple column specifiers with commas: "System.Document.Author,System.Document.Title".

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

No defined and fixed set of properties applies to all documents. For this reason, the SQL asterisk is not permitted in the &lt;columns&gt; setting. For a list of valis Shell system properties, refer to <a href="https://msdn.microsoft.com/library/bb763010(VS.85).aspx">System Properties</a>.

Checkout the <a href="/windows/win32/search/-search-sample-dsearch">DSearch code sample</a> to see how to create a class for a static console application to query Windows Search using the Microsoft.Search.Interop assembly for <a href="/windows/desktop/api/searchapi/nn-searchapi-isearchqueryhelper">ISearchQueryHelper</a>.

## -see-also

<a href="/windows/desktop/api/searchapi/nn-searchapi-isearchqueryhelper">ISearchQueryHelper</a>



<a href="/windows/desktop/api/searchapi/nf-searchapi-isearchqueryhelper-get_queryselectcolumns">ISearchQueryHelper::get_QuerySelectColumns</a>



<a href="/windows/desktop/search/-search-3x-wds-qryidx-overview">Querying the Index Programmatically</a>



<a href="/windows/desktop/search/-search-sql-windowssearch-entry">Querying the Index with Windows Search SQL Syntax</a>



<a href="https://msdn.microsoft.com/library/ff518152(v=VS.85).aspx">System Properties</a>