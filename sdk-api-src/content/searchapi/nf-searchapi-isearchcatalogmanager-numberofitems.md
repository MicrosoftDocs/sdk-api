---
UID: NF:searchapi.ISearchCatalogManager.NumberOfItems
title: ISearchCatalogManager::NumberOfItems
author: windows-sdk-content
description: Gets the number of items in the catalog.
old-location: search\_search_ISearchCatalogManager_NumberOfItems.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\indexmanagement\isearchcatalogmanager\numberofitems.htm
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: ISearchCatalogManager interface [search],NumberOfItems method, ISearchCatalogManager.NumberOfItems, ISearchCatalogManager::NumberOfItems, NumberOfItems, NumberOfItems method [search], NumberOfItems method [search],ISearchCatalogManager interface, _search_ISearchCatalogManager_NumberOfItems, search._search_ISearchCatalogManager_NumberOfItems, searchapi/ISearchCatalogManager::NumberOfItems
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
 - ISearchCatalogManager.NumberOfItems
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
---

# ISearchCatalogManager::NumberOfItems


## -description


Gets the number of items in the catalog.
      


## -parameters




### -param plCount [out, retval]

Type: <b>LONG*</b>

Receives a pointer to the number of items in the catalog.
        


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



