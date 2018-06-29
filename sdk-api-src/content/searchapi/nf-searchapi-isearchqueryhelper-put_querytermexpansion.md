---
UID: NF:searchapi.ISearchQueryHelper.put_QueryTermExpansion
title: ISearchQueryHelper::put_QueryTermExpansion
author: windows-sdk-content
description: Sets a value that specifies how query terms are to be expanded.
old-location: search\_search_ISearchQueryHelper_put_QueryTermExpansion.htm
old-project: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\isearchqueryhelper\put_querytermexpansion.htm
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: ISearchQueryHelper interface [search],put_QueryTermExpansion method, ISearchQueryHelper.put_QueryTermExpansion, ISearchQueryHelper::put_QueryTermExpansion, _search_ISearchQueryHelper_put_QueryTermExpansion, put_QueryTermExpansion, put_QueryTermExpansion method [search], put_QueryTermExpansion method [search],ISearchQueryHelper interface, search._search_ISearchQueryHelper_put_QueryTermExpansion, searchapi/ISearchQueryHelper::put_QueryTermExpansion
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
 - ISearchQueryHelper.put_QueryTermExpansion
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# ISearchQueryHelper::put_QueryTermExpansion


## -description


Sets a value that specifies how query terms are to be expanded.


## -parameters




### -param expandTerms [in]

Type: <b><a href="https://msdn.microsoft.com/library/Aa965705(v=VS.85).aspx">SEARCH_TERM_EXPANSION</a></b>

Value from the <a href="https://msdn.microsoft.com/library/Aa965705(v=VS.85).aspx">SEARCH_TERM_EXPANSION</a> enumeration that specifies the search term expansion. If not set, the default value is SEARCH_TERM_PREFIX_ALL.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The <b>ISearchQueryHelper::put_QueryTermExpansion</b> method allows for expansion of some query terms with wildcard characters, similar to regular expression expansion. 

While the <a href="https://msdn.microsoft.com/library/Aa965705(v=VS.85).aspx">SEARCH_TERM_EXPANSION</a> enumerated type lets you specify stem expansion, Windows Search does not currently support its use with the <a href="https://msdn.microsoft.com/library/Bb231313(v=VS.85).aspx">ISearchQueryHelper</a> interface.

The DSearch code sample, available on <a href="http://go.microsoft.com/fwlink/p/?linkid=155654">Code Gallery</a> and the <a href="http://go.microsoft.com/fwlink/p/?linkid=129787">Windows 7 SDK</a>, demonstrates how to create a class for a static console application to query Windows Search using the Microsoft.Search.Interop assembly for <a href="https://msdn.microsoft.com/library/Bb231313(v=VS.85).aspx">ISearchQueryHelper</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/Bb231313(v=VS.85).aspx">ISearchQueryHelper</a>



<a href="https://msdn.microsoft.com/library/Bb231311(v=VS.85).aspx">ISearchQueryHelper::get_QueryTermExpansion</a>



<a href="https://msdn.microsoft.com/library/Bb266517(v=VS.85).aspx">Querying the Index Programmatically</a>



<a href="https://msdn.microsoft.com/library/Bb231256(v=VS.85).aspx">Querying the Index with Windows Search SQL Syntax</a>



<a href="https://msdn.microsoft.com/library/Aa965705(v=VS.85).aspx">SEARCH_TERM_EXPANSION</a>
 

 

