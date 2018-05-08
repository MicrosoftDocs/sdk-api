---
UID: NF:searchapi.ISearchQueryHelper.get_QueryTermExpansion
title: ISearchQueryHelper::get_QueryTermExpansion
author: windows-driver-content
description: Gets the value that specifies how query terms are to be expanded.
old-location: search\_search_ISearchQueryHelper_get_QueryTermExpansion.htm
old-project: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\isearchqueryhelper\get_querytermexpansion.htm
ms.author: windowsdriverdev
ms.date: 5/4/2018
ms.keywords: ISearchQueryHelper interface [search],get_QueryTermExpansion method, ISearchQueryHelper.get_QueryTermExpansion, ISearchQueryHelper::get_QueryTermExpansion, _search_ISearchQueryHelper_get_QueryTermExpansion, get_QueryTermExpansion, get_QueryTermExpansion method [search], get_QueryTermExpansion method [search],ISearchQueryHelper interface, search._search_ISearchQueryHelper_get_QueryTermExpansion, searchapi/ISearchQueryHelper::get_QueryTermExpansion
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
-	ISearchQueryHelper.get_QueryTermExpansion
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# ISearchQueryHelper::get_QueryTermExpansion


## -description


Gets the value that specifies how query terms are to be expanded.


## -parameters




### -param pExpandTerms [out, retval]

Type: <b><a href="https://msdn.microsoft.com/9259fce0-235b-4629-8b9a-56385ff9f2af">SEARCH_TERM_EXPANSION</a>*</b>

Receives a pointer to a value from the <a href="https://msdn.microsoft.com/9259fce0-235b-4629-8b9a-56385ff9f2af">SEARCH_TERM_EXPANSION</a> enumeration that specifies the query term expansion.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



While the <a href="https://msdn.microsoft.com/9259fce0-235b-4629-8b9a-56385ff9f2af">SEARCH_TERM_EXPANSION</a> enumerated type lets you specify stem expansion, Windows Search does not currently support its use with the <a href="https://msdn.microsoft.com/1e075961-63b7-4d91-b6ea-5d06d5b81140">ISearchQueryHelper</a> interface.

The DSearch code sample, available on <a href="http://go.microsoft.com/fwlink/p/?linkid=155654">Code Gallery</a> and the <a href="http://go.microsoft.com/fwlink/p/?linkid=129787">Windows 7 SDK</a>, demonstrates how to create a class for a static console application to query Windows Search using the Microsoft.Search.Interop assembly for <a href="https://msdn.microsoft.com/1e075961-63b7-4d91-b6ea-5d06d5b81140">ISearchQueryHelper</a>.




## -see-also




<a href="https://msdn.microsoft.com/1e075961-63b7-4d91-b6ea-5d06d5b81140">ISearchQueryHelper</a>



<a href="https://msdn.microsoft.com/edcc8a86-b677-4f84-aa6f-90ada895dbcc">ISearchQueryHelper::put_QueryTermExpansion</a>



<a href="https://msdn.microsoft.com/2c161b7f-4e28-4e8a-add6-3c1cda00a622">Querying the Index Programmatically</a>



<a href="https://msdn.microsoft.com/a2eb550a-bb55-4dbd-9ca1-60b776eb9339">Querying the Index with Windows Search SQL Syntax</a>



<a href="https://msdn.microsoft.com/9259fce0-235b-4629-8b9a-56385ff9f2af">SEARCH_TERM_EXPANSION</a>
 

 

