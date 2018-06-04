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

# ISearchCatalogManager::GetItemsChangedSink


## -description


Gets the change notification sink interface.


## -parameters




### -param pISearchNotifyInlineSite [in]

Type: <b><a href="https://msdn.microsoft.com/5837ccf6-1156-44a5-9135-3e3b47244f9d">ISearchNotifyInlineSite</a>*</b>

A pointer to your <a href="https://msdn.microsoft.com/5837ccf6-1156-44a5-9135-3e3b47244f9d">ISearchNotifyInlineSite</a> interface.


### -param riid [in]

Type: <b>REFIID</b>

The UUID of the <a href="https://msdn.microsoft.com/7ad55cf5-5024-4a30-a465-536fb1429b19">ISearchItemsChangedSink</a> interface.


### -param ppv [out]

Type: <b>void*</b>

Receives a pointer to the <a href="https://msdn.microsoft.com/7ad55cf5-5024-4a30-a465-536fb1429b19">ISearchItemsChangedSink</a> interface.


### -param pGUIDCatalogResetSignature [out]

Type: <b>GUID*</b>

Receives a pointer to the GUID representing the catalog reset. If this GUID changes, all notifications must be resent.


### -param pGUIDCheckPointSignature [out]

Type: <b>GUID*</b>

Receives a pointer to the GUID representing a checkpoint.


### -param pdwLastCheckPointNumber [out]

Type: <b>DWORD*</b>

Receives a pointer to the number indicating the last checkpoint to be saved.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



