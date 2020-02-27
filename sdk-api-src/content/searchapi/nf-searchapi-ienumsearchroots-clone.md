---
UID: NF:searchapi.IEnumSearchRoots.Clone
title: IEnumSearchRoots::Clone (searchapi.h)
description: Creates a copy of the IEnumSearchRoots object with the same contents and state as the current one.
old-location: search\_search_IEnumSearchRoots_Clone.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\crawlscope\ienumsearchroots\clone.htm
ms.date: 12/05/2018
ms.keywords: Clone, Clone method [search], Clone method [search],IEnumSearchRoots interface, IEnumSearchRoots interface [search],Clone method, IEnumSearchRoots.Clone, IEnumSearchRoots::Clone, _search_IEnumSearchRoots_Clone, search._search_IEnumSearchRoots_Clone, searchapi/IEnumSearchRoots::Clone
f1_keywords:
- searchapi/IEnumSearchRoots.Clone
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
req.idl: 
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
- IEnumSearchRoots.Clone
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
---

# IEnumSearchRoots::Clone


## -description


Creates a copy of the <a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nn-searchapi-ienumsearchroots">IEnumSearchRoots</a> object with the same contents and state as the current one.


## -parameters




### -param ppenum [out, retval]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nn-searchapi-ienumsearchroots">IEnumSearchRoots</a>**</b>

Returns a pointer to the new <a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nn-searchapi-ienumsearchroots">IEnumSearchRoots</a> object. The calling application must free the new object by calling its <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> method.
                


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



<b>Windows 7 and later</b>: the CrawlScopeCommandLine code sample, available on <a href="https://code.msdn.microsoft.com/windowssearch">Code Gallery</a> and the <a href="https://msdn.microsoft.com/windowsvista/bb980924.aspx">Windows 7 SDK</a>, demonstrates how to define command line options for Crawl Scope Manager (CSM) indexing operations.
        



