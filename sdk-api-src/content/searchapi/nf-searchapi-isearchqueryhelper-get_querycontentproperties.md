---
UID: NF:searchapi.ISearchQueryHelper.get_QueryContentProperties
title: ISearchQueryHelper::get_QueryContentProperties
author: windows-sdk-content
description: Gets the list of properties included in the query when search terms do not explicitly specify a property.
old-location: search\_search_ISearchQueryHelper_get_QueryContentProperties.htm
old-project: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\isearchqueryhelper\get_querycontentproperties.htm
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: ISearchQueryHelper interface [search],get_QueryContentProperties method, ISearchQueryHelper.get_QueryContentProperties, ISearchQueryHelper::get_QueryContentProperties, _search_ISearchQueryHelper_get_QueryContentProperties, get_QueryContentProperties, get_QueryContentProperties method [search], get_QueryContentProperties method [search],ISearchQueryHelper interface, search._search_ISearchQueryHelper_get_QueryContentProperties, searchapi/ISearchQueryHelper::get_QueryContentProperties
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
 - ISearchQueryHelper.get_QueryContentProperties
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# ISearchQueryHelper::get_QueryContentProperties


## -description


Gets the list of properties included in the query when search terms do not explicitly specify a property.


## -parameters




### -param ppszContentProperties [out, retval]

Type: <b>LPWSTR*</b>

Receives a pointer to a comma-delimited, null-terminated Unicode string of content properties to search. If <i>ppszContentProperties</i> is <b>NULL</b>,  all properties are searched.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Search terms may or may not be explicitly prefixed by a property ("author:Irina" or just "Irina"). If <i>SEARCH_ADVANCED_QUERY_SYNTAX</i> or <i>NO_QUERY_SYNTAX</i> is set in <a href="https://msdn.microsoft.com/4df77a77-10fd-411c-bd35-450ffdbc1da8">ISearchQueryHelper::put_QuerySyntax</a>, all search terms not prefixed by a property keyword are matched against the list of properties in <i>ppszContentProperties</i>.

The DSearch code sample, available on <a href="http://go.microsoft.com/fwlink/p/?linkid=155654">Code Gallery</a> and the <a href="http://go.microsoft.com/fwlink/p/?linkid=129787">Windows 7 SDK</a>, demonstrates how to create a class for a static console application to query Windows Search using the Microsoft.Search.Interop assembly for <a href="https://msdn.microsoft.com/1e075961-63b7-4d91-b6ea-5d06d5b81140">ISearchQueryHelper</a>.




## -see-also




<a href="https://msdn.microsoft.com/1e075961-63b7-4d91-b6ea-5d06d5b81140">ISearchQueryHelper</a>



<a href="https://msdn.microsoft.com/75d4882c-305a-4035-9c8c-e72de3c6812f">ISearchQueryHelper::put_QueryContentProperties</a>



<a href="https://msdn.microsoft.com/2c161b7f-4e28-4e8a-add6-3c1cda00a622">Querying the Index Programmatically</a>



<a href="https://msdn.microsoft.com/a2eb550a-bb55-4dbd-9ca1-60b776eb9339">Querying the Index with Windows Search SQL Syntax</a>



<a href="http://msdn.microsoft.com/en-us/library/ff518152(v=VS.85).aspx">System Properties</a>
 

 

