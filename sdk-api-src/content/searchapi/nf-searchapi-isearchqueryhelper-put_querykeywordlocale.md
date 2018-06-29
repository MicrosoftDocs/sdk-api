---
UID: NF:searchapi.ISearchQueryHelper.put_QueryKeywordLocale
title: ISearchQueryHelper::put_QueryKeywordLocale
author: windows-sdk-content
description: Sets the language code identifier (LCID) for the locale to use when parsing Advanced Query Syntax (AQS) keywords.
old-location: search\_search_ISearchQueryHelper_put_QueryKeywordLocale.htm
old-project: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\isearchqueryhelper\put_querykeywordlocale.htm
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: ISearchQueryHelper interface [search],put_QueryKeywordLocale method, ISearchQueryHelper.put_QueryKeywordLocale, ISearchQueryHelper::put_QueryKeywordLocale, _search_ISearchQueryHelper_put_QueryKeywordLocale, put_QueryKeywordLocale, put_QueryKeywordLocale method [search], put_QueryKeywordLocale method [search],ISearchQueryHelper interface, search._search_ISearchQueryHelper_put_QueryKeywordLocale, searchapi/ISearchQueryHelper::put_QueryKeywordLocale
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
 - ISearchQueryHelper.put_QueryKeywordLocale
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# ISearchQueryHelper::put_QueryKeywordLocale


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



The DSearch code sample, available on <a href="http://go.microsoft.com/fwlink/p/?linkid=155654">Code Gallery</a> and the <a href="http://go.microsoft.com/fwlink/p/?linkid=129787">Windows 7 SDK</a>, demonstrates how to create a class for a static console application to query Windows Search using the Microsoft.Search.Interop assembly for <a href="https://msdn.microsoft.com/library/Bb231313(v=VS.85).aspx">ISearchQueryHelper</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/Bb231313(v=VS.85).aspx">ISearchQueryHelper</a>



<a href="https://msdn.microsoft.com/library/Bb231306(v=VS.85).aspx">ISearchQueryHelper::get_QueryKeywordLocale</a>



<a href="https://msdn.microsoft.com/library/Bb266517(v=VS.85).aspx">Querying the Index Programmatically</a>



<a href="https://msdn.microsoft.com/library/Bb231256(v=VS.85).aspx">Querying the Index with Windows Search SQL Syntax</a>
 

 

