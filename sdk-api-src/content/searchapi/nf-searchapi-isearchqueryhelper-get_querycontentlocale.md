---
UID: NF:searchapi.ISearchQueryHelper.get_QueryContentLocale
title: ISearchQueryHelper::get_QueryContentLocale method
author: windows-driver-content
description: Gets the language code identifier (LCID) for the query.
old-location: search\_search_ISearchQueryHelper_get_QueryContentLocale.htm
old-project: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\isearchqueryhelper\get_querycontentlocale.htm
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: ISearchQueryHelper, ISearchQueryHelper interface [search], get_QueryContentLocale method, ISearchQueryHelper::get_QueryContentLocale, _search_ISearchQueryHelper_get_QueryContentLocale, get_QueryContentLocale method [search], get_QueryContentLocale method [search], ISearchQueryHelper interface, get_QueryContentLocale,ISearchQueryHelper.get_QueryContentLocale, search._search_ISearchQueryHelper_get_QueryContentLocale, searchapi/ISearchQueryHelper::get_QueryContentLocale
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
-	ISearchQueryHelper.get_QueryContentLocale
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# ISearchQueryHelper::get_QueryContentLocale method


## -description


Gets the language code identifier (LCID) for the query.


## -parameters




### -param plcid [out, retval]

Type: <b>LCID*</b>

Receives a pointer to the locale identifier used.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The locale identifier has the components necessary to uniquely identify one of the installed system-defined locales. The locale retrieved is used for word breaking, normalizing, and stemming the string values extracted from the query string. If the locale identifier was not set with <a href="https://msdn.microsoft.com/e444ad37-6bbd-4408-882b-815193a098bf">ISearchQueryHelper::put_QueryContentLocale</a>, the active input locale is retrieved.

The DSearch code sample, available on <a href="http://go.microsoft.com/fwlink/p/?linkid=155654">Code Gallery</a> and the <a href="http://go.microsoft.com/fwlink/p/?linkid=129787">Windows 7 SDK</a>, demonstrates how to create a class for a static console application to query Windows Search using the Microsoft.Search.Interop assembly for <a href="https://msdn.microsoft.com/1e075961-63b7-4d91-b6ea-5d06d5b81140">ISearchQueryHelper</a>.




## -see-also




<a href="https://msdn.microsoft.com/1e075961-63b7-4d91-b6ea-5d06d5b81140">ISearchQueryHelper</a>



<a href="https://msdn.microsoft.com/e444ad37-6bbd-4408-882b-815193a098bf">ISearchQueryHelper::put_QueryContentLocale</a>



<a href="https://msdn.microsoft.com/2c161b7f-4e28-4e8a-add6-3c1cda00a622">Querying the Index Programmatically</a>



<a href="https://msdn.microsoft.com/a2eb550a-bb55-4dbd-9ca1-60b776eb9339">Querying the Index with Windows Search SQL Syntax</a>
 

 

