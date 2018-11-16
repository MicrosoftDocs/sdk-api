---
UID: NF:searchapi.ISearchCatalogManager.GetCrawlScopeManager
title: ISearchCatalogManager::GetCrawlScopeManager
author: windows-sdk-content
description: Gets an ISearchCrawlScopeManager interface for this search catalog.
old-location: search\_search_ISearchCatalogManager_GetCrawlScopeManager.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\indexmanagement\isearchcatalogmanager\getcrawlscopemanager.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetCrawlScopeManager, GetCrawlScopeManager method [search], GetCrawlScopeManager method [search],ISearchCatalogManager interface, ISearchCatalogManager interface [search],GetCrawlScopeManager method, ISearchCatalogManager.GetCrawlScopeManager, ISearchCatalogManager::GetCrawlScopeManager, _search_ISearchCatalogManager_GetCrawlScopeManager, search._search_ISearchCatalogManager_GetCrawlScopeManager, searchapi/ISearchCatalogManager::GetCrawlScopeManager
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: searchapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps only]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Searchapi.h
api_name:
 - ISearchCatalogManager.GetCrawlScopeManager
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
- apiref
: 
- COM
: 
- searchapi.h
: 
- ISearchCatalogManager.GetCrawlScopeManager
: 
---

# ISearchCatalogManager::GetCrawlScopeManager


## -description


Gets an <a href="https://msdn.microsoft.com/en-us/library/Bb266492(v=VS.85).aspx">ISearchCrawlScopeManager</a> interface for this search catalog.
      


## -parameters




### -param ppCrawlScopeManager [out, retval]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb266492(v=VS.85).aspx">ISearchCrawlScopeManager</a>**</b>

Receives a pointer to a new <a href="https://msdn.microsoft.com/en-us/library/Bb266492(v=VS.85).aspx">ISearchCrawlScopeManager</a> interface.
        


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



