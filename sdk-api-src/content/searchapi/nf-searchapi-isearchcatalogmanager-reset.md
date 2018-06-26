---
UID: NF:searchapi.ISearchCatalogManager.Reset
title: ISearchCatalogManager::Reset
author: windows-sdk-content
description: Resets the underlying catalog by rebuilding the databases and performing a full indexing.
old-location: search\_search_ISearchCatalogManager_Reset.htm
old-project: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\indexmanagement\isearchcatalogmanager\reset.htm
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: ISearchCatalogManager interface [search],Reset method, ISearchCatalogManager.Reset, ISearchCatalogManager::Reset, Reset, Reset method [search], Reset method [search],ISearchCatalogManager interface, _search_ISearchCatalogManager_Reset, search._search_ISearchCatalogManager_Reset, searchapi/ISearchCatalogManager::Reset
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
tech.root: 
req.typenames: ROWSETEVENT_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Searchapi.h
api_name:
 - ISearchCatalogManager.Reset
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# ISearchCatalogManager::Reset


## -description


Resets the underlying catalog by rebuilding the databases and performing a full indexing.


## -parameters






## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks




                Resetting can take a very long time, during which little or no information is available to be searched.
            



