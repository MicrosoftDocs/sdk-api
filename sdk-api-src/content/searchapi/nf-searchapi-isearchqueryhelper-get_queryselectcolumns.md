---
UID: NF:searchapi.ISearchQueryHelper.get_QuerySelectColumns
title: ISearchQueryHelper::get_QuerySelectColumns
author: windows-sdk-content
description: Gets the columns (or properties) requested in the SELECT statement of the query.
old-location: search\_search_ISearchQueryHelper_get_QuerySelectColumns.htm
old-project: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\isearchqueryhelper\get_queryselectcolumns.htm
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: ISearchQueryHelper interface [search],get_QuerySelectColumns method, ISearchQueryHelper.get_QuerySelectColumns, ISearchQueryHelper::get_QuerySelectColumns, _search_ISearchQueryHelper_get_QuerySelectColumns, get_QuerySelectColumns, get_QuerySelectColumns method [search], get_QuerySelectColumns method [search],ISearchQueryHelper interface, search._search_ISearchQueryHelper_get_QuerySelectColumns, searchapi/ISearchQueryHelper::get_QuerySelectColumns
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: ROWSETEVENT_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Searchapi.h
api_name:
 - ISearchQueryHelper.get_QuerySelectColumns
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
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

The DSearch code sample, available on <a href="http://go.microsoft.com/fwlink/p/?linkid=155654">Code Gallery</a> and the <a href="http://go.microsoft.com/fwlink/p/?linkid=129787">Windows 7 SDK</a>, demonstrates how to create a class for a static console application to query Windows Search using the Microsoft.Search.Interop assembly for <a href="https://msdn.microsoft.com/1e075961-63b7-4d91-b6ea-5d06d5b81140">ISearchQueryHelper</a>.




## -see-also




<a href="https://msdn.microsoft.com/1e075961-63b7-4d91-b6ea-5d06d5b81140">ISearchQueryHelper</a>



<a href="https://msdn.microsoft.com/99c965a3-6c62-4d86-a007-fb75b5a2bbef">ISearchQueryHelper::put_QuerySelectColumns</a>



<a href="https://msdn.microsoft.com/2c161b7f-4e28-4e8a-add6-3c1cda00a622">Querying the Index Programmatically</a>



<a href="https://msdn.microsoft.com/a2eb550a-bb55-4dbd-9ca1-60b776eb9339">Querying the Index with Windows Search SQL Syntax</a>



<a href="http://msdn.microsoft.com/en-us/library/ff518152(v=VS.85).aspx">System Properties</a>
 

 

