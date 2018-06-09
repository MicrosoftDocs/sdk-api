---
UID: NF:searchapi.ISearchQueryHelper.put_QuerySelectColumns
title: ISearchQueryHelper::put_QuerySelectColumns
author: windows-sdk-content
description: Sets the columns (or properties) requested in the select statement.
old-location: search\_search_ISearchQueryHelper_put_QuerySelectColumns.htm
old-project: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\isearchqueryhelper\put_queryselectcolumns.htm
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: ISearchQueryHelper interface [search],put_QuerySelectColumns method, ISearchQueryHelper.put_QuerySelectColumns, ISearchQueryHelper::put_QuerySelectColumns, _search_ISearchQueryHelper_put_QuerySelectColumns, put_QuerySelectColumns, put_QuerySelectColumns method [search], put_QuerySelectColumns method [search],ISearchQueryHelper interface, search._search_ISearchQueryHelper_put_QuerySelectColumns, searchapi/ISearchQueryHelper::put_QuerySelectColumns
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
 - ISearchQueryHelper.put_QuerySelectColumns
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
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

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



No defined and fixed set of properties applies to all documents. For this reason, the SQL asterisk is not permitted in the &lt;columns&gt; setting. For a list of valis Shell system properties, refer to <a href="http://msdn.microsoft.com/en-us/library/bb763010(VS.85).aspx">System Properties</a>.

The DSearch code sample, available on <a href="http://go.microsoft.com/fwlink/p/?linkid=155654">Code Gallery</a> and the <a href="http://go.microsoft.com/fwlink/p/?linkid=129787">Windows 7 SDK</a>, demonstrates how to create a class for a static console application to query Windows Search using the Microsoft.Search.Interop assembly for <a href="https://msdn.microsoft.com/1e075961-63b7-4d91-b6ea-5d06d5b81140">ISearchQueryHelper</a>.




## -see-also




<a href="https://msdn.microsoft.com/1e075961-63b7-4d91-b6ea-5d06d5b81140">ISearchQueryHelper</a>



<a href="https://msdn.microsoft.com/1496e880-9dd0-40a5-97e7-2a9367bf9127">ISearchQueryHelper::get_QuerySelectColumns</a>



<a href="https://msdn.microsoft.com/2c161b7f-4e28-4e8a-add6-3c1cda00a622">Querying the Index Programmatically</a>



<a href="https://msdn.microsoft.com/a2eb550a-bb55-4dbd-9ca1-60b776eb9339">Querying the Index with Windows Search SQL Syntax</a>



<a href="http://msdn.microsoft.com/en-us/library/ff518152(v=VS.85).aspx">System Properties</a>
 

 

