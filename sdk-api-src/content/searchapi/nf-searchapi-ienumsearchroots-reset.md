---
UID: NF:searchapi.IEnumSearchRoots.Reset
title: IEnumSearchRoots::Reset (searchapi.h)
description: Moves the internal counter to the beginning of the list so a subsequent call to IEnumSearchRoots::Next retrieves from the beginning.
helpviewer_keywords: ["IEnumSearchRoots interface [search]","Reset method","IEnumSearchRoots.Reset","IEnumSearchRoots::Reset","Reset","Reset method [search]","Reset method [search]","IEnumSearchRoots interface","_search_IEnumSearchRoots_Reset","search._search_IEnumSearchRoots_Reset","searchapi/IEnumSearchRoots::Reset"]
old-location: search\_search_IEnumSearchRoots_Reset.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\crawlscope\ienumsearchroots\reset.htm
ms.date: 12/05/2018
ms.keywords: IEnumSearchRoots interface [search],Reset method, IEnumSearchRoots.Reset, IEnumSearchRoots::Reset, Reset, Reset method [search], Reset method [search],IEnumSearchRoots interface, _search_IEnumSearchRoots_Reset, search._search_IEnumSearchRoots_Reset, searchapi/IEnumSearchRoots::Reset
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
f1_keywords:
 - IEnumSearchRoots::Reset
 - searchapi/IEnumSearchRoots::Reset
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
 - IEnumSearchRoots.Reset
---

# IEnumSearchRoots::Reset


## -description

Moves the internal counter to the beginning of the list so a subsequent call to <a href="/windows/desktop/api/searchapi/nf-searchapi-ienumsearchroots-next">IEnumSearchRoots::Next</a> retrieves from the beginning.



## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

<b>Windows 7 and later</b>: Check out the <a href="/windows/win32/search/-search-sample-crawlscopecommandline">CrawlScopeCommandLine code sample</a> to see how to define command line options for Crawl Scope Manager (CSM) indexing operations.
