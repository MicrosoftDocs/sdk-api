---
UID: NF:searchapi.ISearchCatalogManager.Reindex
title: ISearchCatalogManager::Reindex
author: windows-driver-content
description: Re-indexes all URLs in the catalog.
old-location: search\_search_ISearchCatalogManager_Reindex.htm
old-project: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\indexmanagement\isearchcatalogmanager\reindex.htm
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: ISearchCatalogManager interface [search],Reindex method, ISearchCatalogManager.Reindex, ISearchCatalogManager::Reindex, Reindex, Reindex method [search], Reindex method [search],ISearchCatalogManager interface, _search_ISearchCatalogManager_Reindex, search._search_ISearchCatalogManager_Reindex, searchapi/ISearchCatalogManager::Reindex
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
req.typenames: ROWSETEVENT_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Searchapi.h
api_name:
-	ISearchCatalogManager.Reindex
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# ISearchCatalogManager::Reindex


## -description



            Re-indexes all URLs in the catalog.
        


## -parameters






## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks




                Old information remains in the catalog until replaced by new information during re-indexing.
            



