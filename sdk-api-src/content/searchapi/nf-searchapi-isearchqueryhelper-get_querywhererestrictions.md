---
UID: NF:searchapi.ISearchQueryHelper.get_QueryWhereRestrictions
title: ISearchQueryHelper::get_QueryWhereRestrictions
author: windows-sdk-content
description: Gets the restrictions appended to a query in WHERE clauses.
old-location: search\_search_ISearchQueryHelper_get_QueryWhereRestrictions.htm
old-project: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\isearchqueryhelper\get_querywhererestrictions.htm
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: ISearchQueryHelper interface [search],get_QueryWhereRestrictions method, ISearchQueryHelper.get_QueryWhereRestrictions, ISearchQueryHelper::get_QueryWhereRestrictions, _search_ISearchQueryHelper_get_QueryWhereRestrictions, get_QueryWhereRestrictions, get_QueryWhereRestrictions method [search], get_QueryWhereRestrictions method [search],ISearchQueryHelper interface, search._search_ISearchQueryHelper_get_QueryWhereRestrictions, searchapi/ISearchQueryHelper::get_QueryWhereRestrictions
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
req.idl: 
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
 - ISearchQueryHelper.get_QueryWhereRestrictions
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# ISearchQueryHelper::get_QueryWhereRestrictions


## -description


Gets the restrictions appended to a query in WHERE clauses.


## -parameters




### -param ppszRestrictions [out, retval]

Type: <b>LPWSTR*</b>

Receives a pointer to a comma-delimited null-terminated Unicode string that specifies one or more restrictions appended to a query by WHERE clauses.
        


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The DSearch code sample, available on <a href="http://go.microsoft.com/fwlink/p/?linkid=155654">Code Gallery</a> and the <a href="http://go.microsoft.com/fwlink/p/?linkid=129787">Windows 7 SDK</a>, demonstrates how to create a class for a static console application to query Windows Search using the Microsoft.Search.Interop assembly for <a href="https://msdn.microsoft.com/1e075961-63b7-4d91-b6ea-5d06d5b81140">ISearchQueryHelper</a>.




## -see-also




<a href="https://msdn.microsoft.com/1e075961-63b7-4d91-b6ea-5d06d5b81140">ISearchQueryHelper</a>



<a href="https://msdn.microsoft.com/0d7f218f-1abc-4f9a-94f7-bb9311097193">ISearchQueryHelper::put_QueryWhereRestrictions</a>



<a href="https://msdn.microsoft.com/2c161b7f-4e28-4e8a-add6-3c1cda00a622">Querying the Index Programmatically</a>



<a href="https://msdn.microsoft.com/a2eb550a-bb55-4dbd-9ca1-60b776eb9339">Querying the Index with Windows Search SQL Syntax</a>
 

 

