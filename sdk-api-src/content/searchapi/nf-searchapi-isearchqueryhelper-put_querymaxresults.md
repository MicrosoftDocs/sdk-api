---
UID: NF:searchapi.ISearchQueryHelper.put_QueryMaxResults
title: ISearchQueryHelper::put_QueryMaxResults
author: windows-sdk-content
description: Sets the maximum number of results to be returned by a query.
old-location: search\_search_ISearchQueryHelper_put_QueryMaxResults.htm
old-project: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\isearchqueryhelper\put_querymaxresults.htm
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: ISearchQueryHelper interface [search],put_QueryMaxResults method, ISearchQueryHelper.put_QueryMaxResults, ISearchQueryHelper::put_QueryMaxResults, _search_ISearchQueryHelper_put_QueryMaxResults, put_QueryMaxResults, put_QueryMaxResults method [search], put_QueryMaxResults method [search],ISearchQueryHelper interface, search._search_ISearchQueryHelper_put_QueryMaxResults, searchapi/ISearchQueryHelper::put_QueryMaxResults
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
 - ISearchQueryHelper.put_QueryMaxResults
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# ISearchQueryHelper::put_QueryMaxResults


## -description


Sets the maximum number of results to be returned by a query.


## -parameters




### -param cMaxResults [in]

Type: <b>LONG</b>

The maximum number of results to be returned. Negative numbers return all results.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The DSearch code sample, available on <a href="http://go.microsoft.com/fwlink/p/?linkid=155654">Code Gallery</a> and the <a href="http://go.microsoft.com/fwlink/p/?linkid=129787">Windows 7 SDK</a>, demonstrates how to create a class for a static console application to query Windows Search using the Microsoft.Search.Interop assembly for <a href="https://msdn.microsoft.com/1e075961-63b7-4d91-b6ea-5d06d5b81140">ISearchQueryHelper</a>.




## -see-also




<a href="https://msdn.microsoft.com/1e075961-63b7-4d91-b6ea-5d06d5b81140">ISearchQueryHelper</a>



<a href="https://msdn.microsoft.com/c0922d84-e370-484b-b412-065aabbf3db1">ISearchQueryHelper::get_QueryMaxResults</a>



<a href="https://msdn.microsoft.com/2c161b7f-4e28-4e8a-add6-3c1cda00a622">Querying the Index Programmatically</a>



<a href="https://msdn.microsoft.com/a2eb550a-bb55-4dbd-9ca1-60b776eb9339">Querying the Index with Windows Search SQL Syntax</a>
 

 

