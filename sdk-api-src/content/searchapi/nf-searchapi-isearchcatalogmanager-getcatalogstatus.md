---
UID: NF:searchapi.ISearchCatalogManager.GetCatalogStatus
title: ISearchCatalogManager::GetCatalogStatus
author: windows-sdk-content
description: Gets the status of the catalog.
old-location: search\_search_ISearchCatalogManager_GetCatalogStatus.htm
old-project: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\indexmanagement\isearchcatalogmanager\getcatalogstatus.htm
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: GetCatalogStatus, GetCatalogStatus method [search], GetCatalogStatus method [search],ISearchCatalogManager interface, ISearchCatalogManager interface [search],GetCatalogStatus method, ISearchCatalogManager.GetCatalogStatus, ISearchCatalogManager::GetCatalogStatus, _search_ISearchCatalogManager_GetCatalogStatus, search._search_ISearchCatalogManager_GetCatalogStatus, searchapi/ISearchCatalogManager::GetCatalogStatus
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: searchapi.h
req.include-header: 
req.redist: Windows Desktop Search (WDS) 3.0
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
 - ISearchCatalogManager.GetCatalogStatus
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# ISearchCatalogManager::GetCatalogStatus


## -description


Gets the status of the catalog.


## -parameters




### -param pStatus [out]

Type: <b><a href="https://msdn.microsoft.com/33e57e0a-d59b-46b9-8f3b-edb7405020ad">CatalogStatus</a>*</b>

Receives a pointer to a value from the <a href="https://msdn.microsoft.com/33e57e0a-d59b-46b9-8f3b-edb7405020ad">CatalogStatus</a> enumeration. If <i>pStatus</i> is <i>CATALOG_STATUS_PAUSED</i>, further information can be obtained from the <i>pPausedReason</i> parameter.


### -param pPausedReason [out]

Type: <b><a href="https://msdn.microsoft.com/d3f31eab-b587-41f8-9d47-779773e53058">CatalogPausedReason</a>*</b>

Receives a pointer to a value from the <a href="https://msdn.microsoft.com/d3f31eab-b587-41f8-9d47-779773e53058">CatalogPausedReason</a> enumeration describing why the catalog is paused. If the catalog status is not <i>CATALOG_STATUS_PAUSED</i>, this parameter receives the value <i>CATALOG_PAUSED_REASON_NONE</i>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



