---
UID: NF:searchapi.ISearchCatalogManager.GetCrawlScopeManager
title: ISearchCatalogManager::GetCrawlScopeManager
author: windows-sdk-content
description: Gets an ISearchCrawlScopeManager interface for this search catalog.
old-location: search\_search_ISearchCatalogManager_GetCrawlScopeManager.htm
old-project: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\indexmanagement\isearchcatalogmanager\getcrawlscopemanager.htm
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: GetCrawlScopeManager, GetCrawlScopeManager method [search], GetCrawlScopeManager method [search],ISearchCatalogManager interface, ISearchCatalogManager interface [search],GetCrawlScopeManager method, ISearchCatalogManager.GetCrawlScopeManager, ISearchCatalogManager::GetCrawlScopeManager, _search_ISearchCatalogManager_GetCrawlScopeManager, search._search_ISearchCatalogManager_GetCrawlScopeManager, searchapi/ISearchCatalogManager::GetCrawlScopeManager
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: ROWSETEVENT_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Searchapi.h
api_name:
-	ISearchCatalogManager.GetCrawlScopeManager
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# ISearchCatalogManager::GetCrawlScopeManager


## -description



        Gets an <a href="https://msdn.microsoft.com/8b731941-f1f6-402e-8cee-3c493e3c369d">ISearchCrawlScopeManager</a> interface for this search catalog.
      


## -parameters




### -param ppCrawlScopeManager [out, retval]

Type: <b><a href="https://msdn.microsoft.com/8b731941-f1f6-402e-8cee-3c493e3c369d">ISearchCrawlScopeManager</a>**</b>


            Receives a pointer to a new <a href="https://msdn.microsoft.com/8b731941-f1f6-402e-8cee-3c493e3c369d">ISearchCrawlScopeManager</a> interface.
        


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



