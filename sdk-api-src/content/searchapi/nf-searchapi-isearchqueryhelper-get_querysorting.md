---
UID: NF:searchapi.ISearchQueryHelper.get_QuerySorting
title: ISearchQueryHelper::get_QuerySorting
author: windows-driver-content
description: Gets the sort order for the query result set.
old-location: search\_search_ISearchQueryHelper_get_QuerySorting.htm
old-project: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\isearchqueryhelper\get_querysorting.htm
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: ISearchQueryHelper interface [search],get_QuerySorting method, ISearchQueryHelper.get_QuerySorting, ISearchQueryHelper::get_QuerySorting, _search_ISearchQueryHelper_get_QuerySorting, get_QuerySorting, get_QuerySorting method [search], get_QuerySorting method [search],ISearchQueryHelper interface, search._search_ISearchQueryHelper_get_QuerySorting, searchapi/ISearchQueryHelper::get_QuerySorting
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
req.typenames: ROWSETEVENT_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Searchapi.h
api_name:
-	ISearchQueryHelper.get_QuerySorting
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# ISearchQueryHelper::get_QuerySorting


## -description


Gets the sort order for the query result set.


## -parameters




### -param ppszSorting [out, retval]

Type: <b>LPWSTR*</b>

Receives a pointer to a comma-delimited, null-terminated Unicode string representing the sort order.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks




<a href="https://msdn.microsoft.com/7d992fa2-4606-46ca-904c-b45056a9bbc2">Windows Search SQL</a> supports sorting on multiple properties, in either ascending (ASC) or descending (DESC) order on each property. For example, the value pointed to by <i>ppszSorting</i> might contain the following:

<code>System.ItemAuthors ASC, System.ItemDate DESC</code>

The DSearch code sample, available on <a href="http://go.microsoft.com/fwlink/p/?linkid=155654">Code Gallery</a> and the <a href="http://go.microsoft.com/fwlink/p/?linkid=129787">Windows 7 SDK</a>, demonstrates how to create a class for a static console application to query Windows Search using the Microsoft.Search.Interop assembly for <a href="https://msdn.microsoft.com/1e075961-63b7-4d91-b6ea-5d06d5b81140">ISearchQueryHelper</a>.




## -see-also




<a href="https://msdn.microsoft.com/1e075961-63b7-4d91-b6ea-5d06d5b81140">ISearchQueryHelper</a>



<a href="https://msdn.microsoft.com/5ff2978a-3487-432e-84e8-4234a251d8d7">ISearchQueryHelper::put_QuerySorting</a>



<a href="https://msdn.microsoft.com/2c161b7f-4e28-4e8a-add6-3c1cda00a622">Querying the Index Programmatically</a>



<a href="https://msdn.microsoft.com/a2eb550a-bb55-4dbd-9ca1-60b776eb9339">Querying the Index with Windows Search SQL Syntax</a>
 

 

