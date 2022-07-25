---
UID: NF:searchapi.ISearchManager.get_PortNumber
title: ISearchManager::get_PortNumber (searchapi.h)
description: Retrieves the port number used to communicate with the proxy server. This port number is stored in the indexer and is set by the ISearchManager::SetProxy method.
helpviewer_keywords: ["ISearchManager interface [search]","get_PortNumber method","ISearchManager.get_PortNumber","ISearchManager::get_PortNumber","_search_ISearchManager_get_PortNumber","get_PortNumber","get_PortNumber method [search]","get_PortNumber method [search]","ISearchManager interface","search._search_ISearchManager_get_PortNumber","searchapi/ISearchManager::get_PortNumber"]
old-location: search\_search_ISearchManager_get_PortNumber.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\indexmanagement\isearchmanager\get_portnumber.htm
ms.date: 12/05/2018
ms.keywords: ISearchManager interface [search],get_PortNumber method, ISearchManager.get_PortNumber, ISearchManager::get_PortNumber, _search_ISearchManager_get_PortNumber, get_PortNumber, get_PortNumber method [search], get_PortNumber method [search],ISearchManager interface, search._search_ISearchManager_get_PortNumber, searchapi/ISearchManager::get_PortNumber
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
 - ISearchManager::get_PortNumber
 - searchapi/ISearchManager::get_PortNumber
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
 - ISearchManager.get_PortNumber
---

# ISearchManager::get_PortNumber


## -description

Retrieves the port number used to communicate with the proxy server. This port number is stored in the indexer and is set by the <a href="/windows/desktop/api/searchapi/nf-searchapi-isearchmanager-setproxy">ISearchManager::SetProxy</a> method.

## -parameters

### -param pdwPortNumber [out, retval]

Type: <b>DWORD*</b>

Receives a pointer to the port number.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Check out the <a href="/windows/win32/search/-search-sample-reindexmatchingurls">ReindexMatchingUrls code sample</a> to see ways to specify which files to re-index and how set it up.