---
UID: NF:searchapi.ISearchManager.GetCatalog
title: ISearchManager::GetCatalog method
author: windows-driver-content
description: Retrieves a catalog by name and creates a new ISearchCatalogManager object for that catalog.
old-location: search\_search_ISearchManager_GetCatalog.htm
old-project: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\indexmanagement\isearchmanager\getcatalog.htm
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: GetCatalog method [search], GetCatalog method [search], ISearchManager interface, GetCatalog,ISearchManager.GetCatalog, ISearchManager, ISearchManager interface [search], GetCatalog method, ISearchManager::GetCatalog, _search_ISearchManager_GetCatalog, search._search_ISearchManager_GetCatalog, searchapi/ISearchManager::GetCatalog
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
req.idl: Searchadmin.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: ROWSETEVENT_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Searchapi.h
api_name:
-	ISearchManager.GetCatalog
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# ISearchManager::GetCatalog method


## -description



            Retrieves a catalog by name and creates a new <a href="https://msdn.microsoft.com/098e0574-53af-4b52-99e7-659f98b914ae">ISearchCatalogManager</a> object for that catalog.


## -parameters




### -param pszCatalog [in]

Type: <b>LPCWSTR</b>


                    The name of the catalog to be retrieved.
                


### -param ppCatalogManager [out, retval]

Type: <b><a href="https://msdn.microsoft.com/098e0574-53af-4b52-99e7-659f98b914ae">ISearchCatalogManager</a>**</b>


                    Receives the address of a pointer to the <a href="https://msdn.microsoft.com/098e0574-53af-4b52-99e7-659f98b914ae">ISearchCatalogManager</a> object that is named in <i>pszCatalog</i>.
                


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Currently Microsoft Windows Desktop Search (WDS) 3.0 supports only one catalog and it is named SystemIndex.

The ReindexMatchingUrls code sample, available on <a href="http://go.microsoft.com/fwlink/p/?linkid=155654">Code Gallery</a> and the <a href="http://go.microsoft.com/fwlink/p/?linkid=129787">Windows 7 SDK</a>, demonstrates ways to specify which files to re-index and how.



