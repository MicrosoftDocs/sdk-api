---
UID: NF:searchapi.ISearchManager.GetCatalog
title: ISearchManager::GetCatalog (searchapi.h)
description: Retrieves a catalog by name and creates a new ISearchCatalogManager object for that catalog.
helpviewer_keywords: ["GetCatalog","GetCatalog method [search]","GetCatalog method [search]","ISearchManager interface","ISearchManager interface [search]","GetCatalog method","ISearchManager.GetCatalog","ISearchManager::GetCatalog","_search_ISearchManager_GetCatalog","search._search_ISearchManager_GetCatalog","searchapi/ISearchManager::GetCatalog"]
old-location: search\_search_ISearchManager_GetCatalog.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\indexmanagement\isearchmanager\getcatalog.htm
ms.date: 12/05/2018
ms.keywords: GetCatalog, GetCatalog method [search], GetCatalog method [search],ISearchManager interface, ISearchManager interface [search],GetCatalog method, ISearchManager.GetCatalog, ISearchManager::GetCatalog, _search_ISearchManager_GetCatalog, search._search_ISearchManager_GetCatalog, searchapi/ISearchManager::GetCatalog
f1_keywords:
- searchapi/ISearchManager.GetCatalog
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
req.idl: Searchadmin.idl
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
- ISearchManager.GetCatalog
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
---

# ISearchManager::GetCatalog


## -description


Retrieves a catalog by name and creates a new <a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nn-searchapi-isearchcatalogmanager">ISearchCatalogManager</a> object for that catalog.


## -parameters




### -param pszCatalog [in]

Type: <b>LPCWSTR</b>

The name of the catalog to be retrieved.
                


### -param ppCatalogManager [out, retval]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nn-searchapi-isearchcatalogmanager">ISearchCatalogManager</a>**</b>

Receives the address of a pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nn-searchapi-isearchcatalogmanager">ISearchCatalogManager</a> object that is named in <i>pszCatalog</i>.
                


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Currently Microsoft Windows Desktop Search (WDS) 3.0 supports only one catalog and it is named SystemIndex.

The ReindexMatchingUrls code sample, available on <a href="https://code.msdn.microsoft.com/windowssearch">Code Gallery</a> and the <a href="https://msdn.microsoft.com/windowsvista/bb980924.aspx">Windows 7 SDK</a>, demonstrates ways to specify which files to re-index and how.



