---
UID: NF:searchapi.ISearchCatalogManager.URLBeingIndexed
title: ISearchCatalogManager::URLBeingIndexed method
author: windows-driver-content
description: Gets the URL that is currently being indexed. If no indexing is currently in process, pszUrl is set to NULL.
old-location: search\_search_ISearchCatalogManager_URLBeingIndexed.htm
old-project: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\indexmanagement\isearchcatalogmanager\urlbeingindexed.htm
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: ISearchCatalogManager, ISearchCatalogManager interface [search], URLBeingIndexed method, ISearchCatalogManager::URLBeingIndexed, URLBeingIndexed method [search], URLBeingIndexed method [search], ISearchCatalogManager interface, URLBeingIndexed,ISearchCatalogManager.URLBeingIndexed, _search_ISearchCatalogManager_URLBeingIndexed, search._search_ISearchCatalogManager_URLBeingIndexed, searchapi/ISearchCatalogManager::URLBeingIndexed
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
-	ISearchCatalogManager.URLBeingIndexed
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# ISearchCatalogManager::URLBeingIndexed method


## -description



            Gets the URL that is currently being indexed. If no indexing is currently in process, <i>pszUrl</i> is set to <b>NULL</b>.
        


## -parameters




### -param pszUrl [out, retval]

Type: <b>LPWSTR*</b>


                    Receives a pointer to the URL that is currently being indexed.
                


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



