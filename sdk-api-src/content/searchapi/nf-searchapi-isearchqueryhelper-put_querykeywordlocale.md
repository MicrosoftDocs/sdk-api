---
UID: NF:searchapi.ISearchQueryHelper.put_QueryKeywordLocale
title: ISearchQueryHelper::put_QueryKeywordLocale method
author: windows-driver-content
description: Sets the language code identifier (LCID) for the locale to use when parsing Advanced Query Syntax (AQS) keywords.
old-location: search\_search_ISearchQueryHelper_put_QueryKeywordLocale.htm
old-project: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\isearchqueryhelper\put_querykeywordlocale.htm
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: ISearchQueryHelper, ISearchQueryHelper interface [search], put_QueryKeywordLocale method, ISearchQueryHelper::put_QueryKeywordLocale, _search_ISearchQueryHelper_put_QueryKeywordLocale, put_QueryKeywordLocale method [search], put_QueryKeywordLocale method [search], ISearchQueryHelper interface, put_QueryKeywordLocale,ISearchQueryHelper.put_QueryKeywordLocale, search._search_ISearchQueryHelper_put_QueryKeywordLocale, searchapi/ISearchQueryHelper::put_QueryKeywordLocale
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
-	ISearchQueryHelper.put_QueryKeywordLocale
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# ISearchQueryHelper::put_QueryKeywordLocale method


## -description


Sets the language code identifier (LCID) for the locale to use when parsing Advanced Query Syntax (AQS) keywords.


## -parameters




### -param lcid [in]

Type: <b>LCID</b>

Sets the LCID for the locale to use when parsing Advanced Query Syntax (AQS) keywords.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The DSearch code sample, available on <a href="http://go.microsoft.com/fwlink/p/?linkid=155654">Code Gallery</a> and the <a href="http://go.microsoft.com/fwlink/p/?linkid=129787">Windows 7 SDK</a>, demonstrates how to create a class for a static console application to query Windows Search using the Microsoft.Search.Interop assembly for <a href="https://msdn.microsoft.com/1e075961-63b7-4d91-b6ea-5d06d5b81140">ISearchQueryHelper</a>.




## -see-also




<a href="https://msdn.microsoft.com/1e075961-63b7-4d91-b6ea-5d06d5b81140">ISearchQueryHelper</a>



<a href="https://msdn.microsoft.com/a4344d24-cc16-4da8-a70d-1f74e33d551e">ISearchQueryHelper::get_QueryKeywordLocale</a>



<a href="https://msdn.microsoft.com/2c161b7f-4e28-4e8a-add6-3c1cda00a622">Querying the Index Programmatically</a>



<a href="https://msdn.microsoft.com/a2eb550a-bb55-4dbd-9ca1-60b776eb9339">Querying the Index with Windows Search SQL Syntax</a>
 

 

