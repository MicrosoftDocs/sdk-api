---
UID: NF:searchapi.ISearchQueryHelper.put_QueryWhereRestrictions
title: ISearchQueryHelper::put_QueryWhereRestrictions
author: windows-sdk-content
description: Sets the restrictions appended to a query in WHERE clauses.
old-location: search\_search_ISearchQueryHelper_put_QueryWhereRestrictions.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\isearchqueryhelper\put_querywhererestrictions.htm
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: ISearchQueryHelper interface [search],put_QueryWhereRestrictions method, ISearchQueryHelper.put_QueryWhereRestrictions, ISearchQueryHelper::put_QueryWhereRestrictions, _search_ISearchQueryHelper_put_QueryWhereRestrictions, put_QueryWhereRestrictions, put_QueryWhereRestrictions method [search], put_QueryWhereRestrictions method [search],ISearchQueryHelper interface, search._search_ISearchQueryHelper_put_QueryWhereRestrictions, searchapi/ISearchQueryHelper::put_QueryWhereRestrictions
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
 - ISearchQueryHelper.put_QueryWhereRestrictions
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
---

# ISearchQueryHelper::put_QueryWhereRestrictions


## -description


Sets the restrictions appended to a query in WHERE clauses.


## -parameters




### -param pszRestrictions [in]

Type: <b>LPCWSTR</b>

Pointer to a comma-delimited null-terminated Unicode string that specifies one or more query restrictions appended to the query in generated WHERE clause.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



<i>pszRestrictions</i> must be a valid WHERE clause for Windows Search SQL (without the WHERE keyword).

When you create <i>pszRestrictions</i> with multiple restrictions, additional "WHERE" clauses concatenated to the first must start with "AND" or "OR". For example: "and contains(*, 'qqq')"

The DSearch code sample, available on <a href="http://go.microsoft.com/fwlink/p/?linkid=155654">Code Gallery</a> and the <a href="http://go.microsoft.com/fwlink/p/?linkid=129787">Windows 7 SDK</a>, demonstrates how to create a class for a static console application to query Windows Search using the Microsoft.Search.Interop assembly for <a href="https://msdn.microsoft.com/en-us/library/Bb231313(v=VS.85).aspx">ISearchQueryHelper</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb231313(v=VS.85).aspx">ISearchQueryHelper</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb231312(v=VS.85).aspx">ISearchQueryHelper::get_QueryWhereRestrictions</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb266517(v=VS.85).aspx">Querying the Index Programmatically</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb231256(v=VS.85).aspx">Querying the Index with Windows Search SQL Syntax</a>
 

 

