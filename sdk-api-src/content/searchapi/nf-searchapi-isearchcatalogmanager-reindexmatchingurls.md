---
UID: NF:searchapi.ISearchCatalogManager.ReindexMatchingURLs
title: ISearchCatalogManager::ReindexMatchingURLs (searchapi.h)
description: Reindexes all items that match the provided pattern. This method was not implemented prior to Windows 7.
helpviewer_keywords: ["ISearchCatalogManager interface [search]","ReindexMatchingURLs method","ISearchCatalogManager.ReindexMatchingURLs","ISearchCatalogManager::ReindexMatchingURLs","ReindexMatchingURLs","ReindexMatchingURLs method [search]","ReindexMatchingURLs method [search]","ISearchCatalogManager interface","_search_ISearchCatalogManager_ReindexMatchingURLs","search._search_ISearchCatalogManager_ReindexMatchingURLs","searchapi/ISearchCatalogManager::ReindexMatchingURLs"]
old-location: search\_search_ISearchCatalogManager_ReindexMatchingURLs.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\indexmanagement\isearchcatalogmanager\reindexmatchingurls.htm
ms.date: 12/05/2018
ms.keywords: ISearchCatalogManager interface [search],ReindexMatchingURLs method, ISearchCatalogManager.ReindexMatchingURLs, ISearchCatalogManager::ReindexMatchingURLs, ReindexMatchingURLs, ReindexMatchingURLs method [search], ReindexMatchingURLs method [search],ISearchCatalogManager interface, _search_ISearchCatalogManager_ReindexMatchingURLs, search._search_ISearchCatalogManager_ReindexMatchingURLs, searchapi/ISearchCatalogManager::ReindexMatchingURLs
req.header: searchapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista, Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Searchcatalog.idl
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
 - ISearchCatalogManager::ReindexMatchingURLs
 - searchapi/ISearchCatalogManager::ReindexMatchingURLs
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
 - ISearchCatalogManager.ReindexMatchingURLs
---

# ISearchCatalogManager::ReindexMatchingURLs


## -description

Reindexes all items that match the provided pattern. This method was not implemented prior to Windows 7.

## -parameters

### -param pszPattern [in]

Type: <b>LPCWSTR</b>

A pointer to the pattern to be matched for reindexing. The pattern can be a standard pattern such as <code>*.pdf</code> or a pattern in the form of a URL such as <code>file:///c:\MyStuff\*.pdf</code>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method is fully implemented for Windows 7.

