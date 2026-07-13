---
UID: NF:searchapi.ISearchManager.GetIndexerVersionStr
title: ISearchManager::GetIndexerVersionStr (searchapi.h)
description: Retrieves the version of the current indexer as a single string.
helpviewer_keywords: ["GetIndexerVersionStr","GetIndexerVersionStr method [search]","GetIndexerVersionStr method [search]","ISearchManager interface","ISearchManager interface [search]","GetIndexerVersionStr method","ISearchManager.GetIndexerVersionStr","ISearchManager::GetIndexerVersionStr","WDS 2.65 on Windows XP/Windows Server 2003","WDS 2.66 on Windows XP/Windows Server 2003","WDS 3.0 on Windows XP/Windows Server 2003","WDS 3.01 on Windows XP/Windows Server 2003","Windows Search 4.0 Preview on all platforms","Windows Search 4.0 on all platforms","Windows Search on Windows Vista RTM/Windows Server RTM","Windows Search on Windows Vista SP1/Windows Server 2008","_search_ISearchManager_GetIndexerVersionStr","search._search_ISearchManager_GetIndexerVersionStr","searchapi/ISearchManager::GetIndexerVersionStr"]
old-location: search\_search_ISearchManager_GetIndexerVersionStr.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\indexmanagement\isearchmanager\getindexerversionstr.htm
ms.date: 12/05/2018
ms.keywords: GetIndexerVersionStr, GetIndexerVersionStr method [search], GetIndexerVersionStr method [search],ISearchManager interface, ISearchManager interface [search],GetIndexerVersionStr method, ISearchManager.GetIndexerVersionStr, ISearchManager::GetIndexerVersionStr, WDS 2.65 on Windows XP/Windows Server 2003, WDS 2.66 on Windows XP/Windows Server 2003, WDS 3.0 on Windows XP/Windows Server 2003, WDS 3.01 on Windows XP/Windows Server 2003, Windows Search 4.0 Preview on all platforms, Windows Search 4.0 on all platforms, Windows Search on Windows Vista RTM/Windows Server RTM, Windows Search on Windows Vista SP1/Windows Server 2008, _search_ISearchManager_GetIndexerVersionStr, search._search_ISearchManager_GetIndexerVersionStr, searchapi/ISearchManager::GetIndexerVersionStr
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
 - ISearchManager::GetIndexerVersionStr
 - searchapi/ISearchManager::GetIndexerVersionStr
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
 - ISearchManager.GetIndexerVersionStr
---

# ISearchManager::GetIndexerVersionStr


## -description

Retrieves the version of the current indexer as a single string.

## -parameters

### -param ppszVersionString [out]

Type: <b>LPWSTR*</b>

Receives the version of the current indexer.



##### 65 on Windows XP/Windows Server 2003

02.06.5000.5378



##### 66 on Windows XP/Windows Server 2003

02.06.6000.5414



##### 0 on Windows XP/Windows Server 2003

03.00.5824.280



##### 01 on Windows XP/Windows Server 2003

03.01.6000.72



#### Windows Search on Windows Vista RTM/Windows Server RTM

03.00.6000.16386



#### Windows Search on Windows Vista SP1/Windows Server 2008

03.00.6001.18000



##### 0 Preview on all platforms

04.00.6001.381



##### 0 on all platforms

04.00.6001.16503

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Check out the <a href="/windows/win32/search/-search-sample-reindexmatchingurls">ReindexMatchingUrls code sample</a> to see ways to specify which files to re-index and how set it up.