---
UID: NF:searchapi.ISearchManager.GetIndexerVersion
title: ISearchManager::GetIndexerVersion (searchapi.h)
description: Retrieves the version of the current indexer in two chunks:\_the major version signifier and the minor version signifier.
helpviewer_keywords: ["GetIndexerVersion","GetIndexerVersion method [search]","GetIndexerVersion method [search]","ISearchManager interface","ISearchManager interface [search]","GetIndexerVersion method","ISearchManager.GetIndexerVersion","ISearchManager::GetIndexerVersion","_search_ISearchManager_GetIndexerVersion","search._search_ISearchManager_GetIndexerVersion","searchapi/ISearchManager::GetIndexerVersion"]
old-location: search\_search_ISearchManager_GetIndexerVersion.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\indexmanagement\isearchmanager\getindexerversion.htm
ms.date: 12/05/2018
ms.keywords: GetIndexerVersion, GetIndexerVersion method [search], GetIndexerVersion method [search],ISearchManager interface, ISearchManager interface [search],GetIndexerVersion method, ISearchManager.GetIndexerVersion, ISearchManager::GetIndexerVersion, _search_ISearchManager_GetIndexerVersion, search._search_ISearchManager_GetIndexerVersion, searchapi/ISearchManager::GetIndexerVersion
req.header: searchapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Searchadmin.idl
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
 - ISearchManager::GetIndexerVersion
 - searchapi/ISearchManager::GetIndexerVersion
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
 - ISearchManager.GetIndexerVersion
---

# ISearchManager::GetIndexerVersion


## -description

Retrieves the version of the current indexer in two chunks: the major version signifier and the minor version signifier.

## -parameters

### -param pdwMajor [out]

Type: <b>DWORD*</b>

Receives the major version signifier (the number to the left of the dot).

### -param pdwMinor [out]

Type: <b>DWORD*</b>

Receives the minor version signifier (the number to the right of the dot).

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Check out the <a href="/windows/win32/search/-search-sample-reindexmatchingurls">ReindexMatchingUrls code sample</a> to see ways to specify which files to re-index and how set it up.