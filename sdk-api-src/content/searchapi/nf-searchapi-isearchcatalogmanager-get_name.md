---
UID: NF:searchapi.ISearchCatalogManager.get_Name
title: ISearchCatalogManager::get_Name method
author: windows-driver-content
description: Gets the name of the current catalog.
old-location: search\_search_ISearchCatalogManager_get_Name.htm
old-project: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\indexmanagement\isearchcatalogmanager\get_name.htm
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: ISearchCatalogManager, ISearchCatalogManager interface [search], get_Name method, ISearchCatalogManager::get_Name, _search_ISearchCatalogManager_get_Name, get_Name method [search], get_Name method [search], ISearchCatalogManager interface, get_Name,ISearchCatalogManager.get_Name, search._search_ISearchCatalogManager_get_Name, searchapi/ISearchCatalogManager::get_Name
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
-	ISearchCatalogManager.get_Name
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# ISearchCatalogManager::get_Name method


## -description


Gets the name of the current catalog.


## -parameters




### -param pszName [out, retval]

Type: <b>LPCWSTR*</b>

Receives a pointer to a null-terminated Unicode buffer that contains the name of the current catalog.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



