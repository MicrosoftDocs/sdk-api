---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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



