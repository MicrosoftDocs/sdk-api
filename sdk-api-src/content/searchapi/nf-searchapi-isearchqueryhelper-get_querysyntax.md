---
UID: NF:searchapi.ISearchQueryHelper.get_QuerySyntax
title: ISearchQueryHelper::get_QuerySyntax method
author: windows-driver-content
description: Gets the syntax of the query.
old-location: search\_search_ISearchQueryHelper_get_QuerySyntax.htm
old-project: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\isearchqueryhelper\get_querysyntax.htm
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: ISearchQueryHelper, ISearchQueryHelper interface [search], get_QuerySyntax method, ISearchQueryHelper::get_QuerySyntax, _search_ISearchQueryHelper_get_QuerySyntax, get_QuerySyntax method [search], get_QuerySyntax method [search], ISearchQueryHelper interface, get_QuerySyntax,ISearchQueryHelper.get_QuerySyntax, search._search_ISearchQueryHelper_get_QuerySyntax, searchapi/ISearchQueryHelper::get_QuerySyntax
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
req.idl: 
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
-	ISearchQueryHelper.get_QuerySyntax
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# ISearchQueryHelper::get_QuerySyntax method


## -description


Gets the syntax of the query.


## -parameters




### -param pQuerySyntax [out, retval]

Type: <b><a href="https://msdn.microsoft.com/a0331339-9df0-4190-b7ae-977572b49c2d">SEARCH_QUERY_SYNTAX</a>*</b>

Receives a pointer to a value from the <a href="https://msdn.microsoft.com/a0331339-9df0-4190-b7ae-977572b49c2d">SEARCH_QUERY_SYNTAX</a> enumeration. 


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The allowed syntaxes are Simple, Natural Query Syntax (NQS), and Advanced Query Syntax (AQS). If not set, the default query syntax is SEARCH_ADVANCED_QUERY_SYNTAX.

The DSearch code sample, available on <a href="http://go.microsoft.com/fwlink/p/?linkid=155654">Code Gallery</a> and the <a href="http://go.microsoft.com/fwlink/p/?linkid=129787">Windows 7 SDK</a>, demonstrates how to create a class for a static console application to query Windows Search using the Microsoft.Search.Interop assembly for <a href="https://msdn.microsoft.com/1e075961-63b7-4d91-b6ea-5d06d5b81140">ISearchQueryHelper</a>.




## -see-also




<a href="https://msdn.microsoft.com/1e075961-63b7-4d91-b6ea-5d06d5b81140">ISearchQueryHelper</a>



<a href="https://msdn.microsoft.com/4df77a77-10fd-411c-bd35-450ffdbc1da8">ISearchQueryHelper::put_QuerySyntax</a>



<a href="https://msdn.microsoft.com/2c161b7f-4e28-4e8a-add6-3c1cda00a622">Querying the Index Programmatically</a>



<a href="https://msdn.microsoft.com/a2eb550a-bb55-4dbd-9ca1-60b776eb9339">Querying the Index with Windows Search SQL Syntax</a>
 

 

