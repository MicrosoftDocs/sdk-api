---
UID: NF:searchapi.ISearchQueryHelper.get_ConnectionString
title: ISearchQueryHelper::get_ConnectionString (searchapi.h)
description: Returns the OLE DB connection string for the Window Search index.
helpviewer_keywords: ["ISearchQueryHelper interface [search]","get_ConnectionString method","ISearchQueryHelper.get_ConnectionString","ISearchQueryHelper::get_ConnectionString","_search_ISearchQueryHelper_get_ConnectionString","get_ConnectionString","get_ConnectionString method [search]","get_ConnectionString method [search]","ISearchQueryHelper interface","search._search_ISearchQueryHelper_get_ConnectionString","searchapi/ISearchQueryHelper::get_ConnectionString"]
old-location: search\_search_ISearchQueryHelper_get_ConnectionString.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\isearchqueryhelper\get_connectionstring.htm
ms.date: 12/05/2018
ms.keywords: ISearchQueryHelper interface [search],get_ConnectionString method, ISearchQueryHelper.get_ConnectionString, ISearchQueryHelper::get_ConnectionString, _search_ISearchQueryHelper_get_ConnectionString, get_ConnectionString, get_ConnectionString method [search], get_ConnectionString method [search],ISearchQueryHelper interface, search._search_ISearchQueryHelper_get_ConnectionString, searchapi/ISearchQueryHelper::get_ConnectionString
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
 - ISearchQueryHelper::get_ConnectionString
 - searchapi/ISearchQueryHelper::get_ConnectionString
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
 - ISearchQueryHelper.get_ConnectionString
---

# ISearchQueryHelper::get_ConnectionString


## -description

Returns the OLE DB connection string for the Window Search index.

## -parameters

### -param pszConnectionString [out, retval]

Type: <b>LPWSTR*</b>

Receives a pointer to a null-terminated Unicode string that is a valid OLE DB connection string. This connection string can be used to initialize a connection to the Windows Search index and submit the SQL query returned by  <a href="/windows/desktop/api/searchapi/nf-searchapi-isearchqueryhelper-generatesqlfromuserquery">ISearchQueryHelper::GenerateSQLFromUserQuery</a>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

A connection string is a string version of the initialization properties needed to connect to a data store. The string can include such things as a data source, data source name, or user ID and password.

Checkout the <a href="/windows/win32/search/-search-sample-dsearch">DSearch code sample</a> to see how to create a class for a static console application to query Windows Search using the Microsoft.Search.Interop assembly for <a href="/windows/desktop/api/searchapi/nn-searchapi-isearchqueryhelper">ISearchQueryHelper</a>.

## -see-also

<a href="/windows/desktop/api/searchapi/nn-searchapi-isearchqueryhelper">ISearchQueryHelper</a>



<a href="/windows/desktop/search/-search-3x-wds-qryidx-overview">Querying the Index Programmatically</a>



<a href="/windows/desktop/search/-search-sql-windowssearch-entry">Querying the Index with Windows Search SQL Syntax</a>