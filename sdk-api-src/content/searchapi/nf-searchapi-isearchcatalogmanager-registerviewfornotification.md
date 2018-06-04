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

# ISearchCatalogManager::RegisterViewForNotification


## -description


Not implemented.


## -parameters




### -param pszView [in]

Type: <b>LPCWSTR</b>

A pointer to the name of the view.


### -param pViewChangedSink [in]

Type: <b><a href="https://msdn.microsoft.com/7dabc572-50ef-4a21-be77-2eb780610844">ISearchViewChangedSink</a>*</b>

Pointer to the <a href="https://msdn.microsoft.com/7dabc572-50ef-4a21-be77-2eb780610844">ISearchViewChangedSink</a> object to receive notifications.


### -param pdwCookie [out]

Type: <b>DWORD*</b>


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



