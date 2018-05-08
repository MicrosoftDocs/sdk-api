---
UID: NF:searchapi.ISearchQueryHelper.get_QueryKeywordLocale
title: ISearchQueryHelper::get_QueryKeywordLocale
author: windows-driver-content
description: Gets the language code identifier (LCID) for the locale to use when parsing Advanced Query Syntax (AQS) keywords.
old-location: search\_search_ISearchQueryHelper_get_QueryKeywordLocale.htm
old-project: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\isearchqueryhelper\get_querykeywordlocale.htm
ms.author: windowsdriverdev
ms.date: 5/4/2018
ms.keywords: ISearchQueryHelper interface [search],get_QueryKeywordLocale method, ISearchQueryHelper.get_QueryKeywordLocale, ISearchQueryHelper::get_QueryKeywordLocale, _search_ISearchQueryHelper_get_QueryKeywordLocale, get_QueryKeywordLocale, get_QueryKeywordLocale method [search], get_QueryKeywordLocale method [search],ISearchQueryHelper interface, search._search_ISearchQueryHelper_get_QueryKeywordLocale, searchapi/ISearchQueryHelper::get_QueryKeywordLocale
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
-	ISearchQueryHelper.get_QueryKeywordLocale
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# ISearchQueryHelper::get_QueryKeywordLocale


## -description


Gets the language code identifier (LCID) for the locale to use when parsing Advanced Query Syntax (AQS) keywords.


## -parameters




### -param plcid [out, retval]

Type: <b>LCID*</b>

Receives a pointer to the LCID for the locale to use when parsing Advanced Query Syntax (AQS) keywords.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The DSearch code sample, available on <a href="http://go.microsoft.com/fwlink/p/?linkid=155654">Code Gallery</a> and the <a href="http://go.microsoft.com/fwlink/p/?linkid=129787">Windows 7 SDK</a>, demonstrates how to create a class for a static console application to query Windows Search using the Microsoft.Search.Interop assembly for <a href="https://msdn.microsoft.com/1e075961-63b7-4d91-b6ea-5d06d5b81140">ISearchQueryHelper</a>.




## -see-also




<a href="https://msdn.microsoft.com/1e075961-63b7-4d91-b6ea-5d06d5b81140">ISearchQueryHelper</a>



<a href="https://msdn.microsoft.com/6530db1a-260a-4925-be4a-549e42464983">ISearchQueryHelper::put_QueryKeywordLocale</a>



<a href="https://msdn.microsoft.com/2c161b7f-4e28-4e8a-add6-3c1cda00a622">Querying the Index Programmatically</a>



<a href="https://msdn.microsoft.com/a2eb550a-bb55-4dbd-9ca1-60b776eb9339">Querying the Index with Windows Search SQL Syntax</a>
 

 

