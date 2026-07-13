---
UID: NF:searchapi.ISearchManager.GetParameter
title: ISearchManager::GetParameter (searchapi.h)
description: Not supported.This method returns E_INVALIDARG when called. (ISearchManager.GetParameter)
helpviewer_keywords: ["GetParameter","GetParameter method [search]","GetParameter method [search]","ISearchManager interface","ISearchManager interface [search]","GetParameter method","ISearchManager.GetParameter","ISearchManager::GetParameter","_search_ISearchManager_GetParameter","search._search_ISearchManager_GetParameter","searchapi/ISearchManager::GetParameter"]
old-location: search\_search_ISearchManager_GetParameter.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\indexmanagement\isearchmanager\getparameter.htm
ms.date: 12/05/2018
ms.keywords: GetParameter, GetParameter method [search], GetParameter method [search],ISearchManager interface, ISearchManager interface [search],GetParameter method, ISearchManager.GetParameter, ISearchManager::GetParameter, _search_ISearchManager_GetParameter, search._search_ISearchManager_GetParameter, searchapi/ISearchManager::GetParameter
req.header: searchapi.h
req.include-header: Searchapi.h
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
 - ISearchManager::GetParameter
 - searchapi/ISearchManager::GetParameter
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - searchapi.h
api_name:
 - ISearchManager.GetParameter
---

# ISearchManager::GetParameter


## -description

Not supported.

This method returns E_INVALIDARG when called.

## -parameters

### -param pszName [in]

Type: <b>LPCWSTR</b>

There are currently no valid parameters in this version of search (WDS 3.0).

### -param ppValue [out, retval]

Type: <b><a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a>**</b>

Returns a value in an undefined state as there are no properties currently defined to retrieve values from.

## -returns

Type: <b>HRESULT</b>

This method returns E_InvalidArg as an error code when called.

## -remarks

Check out the <a href="/windows/win32/search/-search-sample-reindexmatchingurls">ReindexMatchingUrls code sample</a> to see ways to specify which files to re-index and how set it up.
