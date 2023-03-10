---
UID: NF:searchapi.IEnumSearchScopeRules.Skip
title: IEnumSearchScopeRules::Skip (searchapi.h)
description: Skips the specified number of elements. (IEnumSearchScopeRules.Skip)
helpviewer_keywords: ["IEnumSearchScopeRules interface [search]","Skip method","IEnumSearchScopeRules.Skip","IEnumSearchScopeRules::Skip","Skip","Skip method [search]","Skip method [search]","IEnumSearchScopeRules interface","_search_IEnumSearchScopeRules_Skip","search._search_IEnumSearchScopeRules_Skip","searchapi/IEnumSearchScopeRules::Skip"]
old-location: search\_search_IEnumSearchScopeRules_Skip.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\crawlscope\ienumsearchscoperules\skip.htm
ms.date: 12/05/2018
ms.keywords: IEnumSearchScopeRules interface [search],Skip method, IEnumSearchScopeRules.Skip, IEnumSearchScopeRules::Skip, Skip, Skip method [search], Skip method [search],IEnumSearchScopeRules interface, _search_IEnumSearchScopeRules_Skip, search._search_IEnumSearchScopeRules_Skip, searchapi/IEnumSearchScopeRules::Skip
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IEnumSearchScopeRules::Skip
 - searchapi/IEnumSearchScopeRules::Skip
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Searchapi.h
api_name:
 - IEnumSearchScopeRules.Skip
---

# IEnumSearchScopeRules::Skip


## -description

Skips the specified number of elements.

## -parameters

### -param celt [in]

Type: <b>ULONG</b>

The number of elements to skip.

## -returns

Type: <b>HRESULT</b>

Returns S_OK if successful, S_FALSE if there were not enough items left in the enumeration to skip, or an error value.

## -remarks

Moves the internal counter a specified number of elements forward so that a subsequent call to <a href="/windows/desktop/api/searchapi/nf-searchapi-ienumsearchscoperules-next">IEnumSearchScopeRules::Next</a> starts from that number.

<b>Windows 7 and later</b>: Check out the <a href="/windows/win32/search/-search-sample-crawlscopecommandline">CrawlScopeCommandLine code sample</a> to see how to define command line options for Crawl Scope Manager (CSM) indexing operations.
