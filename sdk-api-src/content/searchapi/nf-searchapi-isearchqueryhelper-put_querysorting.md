---
UID: NF:searchapi.ISearchQueryHelper.put_QuerySorting
title: ISearchQueryHelper::put_QuerySorting
author: windows-sdk-content
description: Sets the sort order for the query result set.
old-location: search\_search_ISearchQueryHelper_put_QuerySorting.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\isearchqueryhelper\put_querysorting.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ISearchQueryHelper interface [search],put_QuerySorting method, ISearchQueryHelper.put_QuerySorting, ISearchQueryHelper::put_QuerySorting, _search_ISearchQueryHelper_put_QuerySorting, put_QuerySorting, put_QuerySorting method [search], put_QuerySorting method [search],ISearchQueryHelper interface, search._search_ISearchQueryHelper_put_QuerySorting, searchapi/ISearchQueryHelper::put_QuerySorting
ms.prod: windows-hardware
ms.technology: windows-devices
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
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



<i>ppszSorting</i> must be a valid ORDER BY clause (without the ORDER BY keyword). <a href="https://msdn.microsoft.com/7d992fa2-4606-46ca-904c-b45056a9bbc2">Windows Search SQL</a> supports sorting on multiple properties, in either ascending (ASC) or descending (DESC) order on each property. For example, <i>ppszSorting</i> might contain the following:

<code>System.ItemAuthors ASC, System.ItemDate DESC</code>

The DSearch code sample, available on <a href="http://go.microsoft.com/fwlink/p/?linkid=155654">Code Gallery</a> and the <a href="http://go.microsoft.com/fwlink/p/?linkid=129787">Windows 7 SDK</a>, demonstrates how to create a class for a static console application to query Windows Search using the Microsoft.Search.Interop assembly for <a href="https://msdn.microsoft.com/1e075961-63b7-4d91-b6ea-5d06d5b81140">ISearchQueryHelper</a>.




## -see-also




<a href="https://msdn.microsoft.com/1e075961-63b7-4d91-b6ea-5d06d5b81140">ISearchQueryHelper</a>



<a href="https://msdn.microsoft.com/7539d055-bff9-436c-abd1-11e2ff5ed858">ISearchQueryHelper::get_QuerySorting</a>



<a href="https://msdn.microsoft.com/2c161b7f-4e28-4e8a-add6-3c1cda00a622">Querying the Index Programmatically</a>



<a href="https://msdn.microsoft.com/a2eb550a-bb55-4dbd-9ca1-60b776eb9339">Querying the Index with Windows Search SQL Syntax</a>
 

 

