---
UID: NF:searchapi.IEnumSearchScopeRules.Next
title: IEnumSearchScopeRules::Next (searchapi.h)
description: Retrieves the specified number of ISearchScopeRule elements.helpviewer_keywords: ["IEnumSearchScopeRules interface [search]","Next method","IEnumSearchScopeRules.Next","IEnumSearchScopeRules::Next","Next","Next method [search]","Next method [search]","IEnumSearchScopeRules interface","_search_IEnumSearchScopeRules_Next","search._search_IEnumSearchScopeRules_Next","searchapi/IEnumSearchScopeRules::Next"]
old-location: search\_search_IEnumSearchScopeRules_Next.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\crawlscope\ienumsearchscoperules\next.htm
ms.date: 12/05/2018
ms.keywords: IEnumSearchScopeRules interface [search],Next method, IEnumSearchScopeRules.Next, IEnumSearchScopeRules::Next, Next, Next method [search], Next method [search],IEnumSearchScopeRules interface, _search_IEnumSearchScopeRules_Next, search._search_IEnumSearchScopeRules_Next, searchapi/IEnumSearchScopeRules::Next
f1_keywords:
- searchapi/IEnumSearchScopeRules.Next
dev_langs:
- c++
req.header: searchapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Searchapi.idl
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
- IEnumSearchScopeRules.Next
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEnumSearchScopeRules::Next


## -description


Retrieves the specified number of <a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nn-searchapi-isearchscoperule">ISearchScopeRule</a> elements.


## -parameters




### -param celt [in]

Type: <b>ULONG</b>

The number of elements to retrieve.


### -param pprgelt [out]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nn-searchapi-isearchscoperule">ISearchScopeRule</a>**</b>

On return, contains a pointer to an array of <a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nn-searchapi-isearchscoperule">ISearchScopeRule</a> elements.


### -param pceltFetched [in, out]

Type: <b>ULONG*</b>

On return, contains a pointer to the actual number of elements retrieved. Can be <b>NULL</b> if <i>celt</i> == 1, otherwise it must not be <b>NULL</b>.


## -returns



Type: <b>HRESULT</b>

Returns S_OK if successful, S_FALSE if there were not enough items left in the enumeration to be returned, or an error value.




## -remarks



Internally, this method updates a counter to move forward the number of elements actually retrieved; subsequent calls to <b>IEnumSearchScopeRules::Next</b> will start from that number.

<b>Windows 7 and later</b>: the CrawlScopeCommandLine code sample, available on <a href="https://code.msdn.microsoft.com/windowssearch">Code Gallery</a> and the <a href="https://msdn.microsoft.com/windowsvista/bb980924.aspx">Windows 7 SDK</a>, demonstrates how to define command line options for Crawl Scope Manager (CSM) indexing operations.



