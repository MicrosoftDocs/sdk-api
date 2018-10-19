---
UID: NF:searchapi.ISearchCatalogManager.GetItemsChangedSink
title: ISearchCatalogManager::GetItemsChangedSink
author: windows-sdk-content
description: Gets the change notification sink interface.
old-location: search\_search_ISearchCatalogManager_GetItemsChangedSink.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\indexmanagement\isearchcatalogmanager\getitemschangedsink.htm
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: GetItemsChangedSink, GetItemsChangedSink method [search], GetItemsChangedSink method [search],ISearchCatalogManager interface, ISearchCatalogManager interface [search],GetItemsChangedSink method, ISearchCatalogManager.GetItemsChangedSink, ISearchCatalogManager::GetItemsChangedSink, _search_ISearchCatalogManager_GetItemsChangedSink, search._search_ISearchCatalogManager_GetItemsChangedSink, searchapi/ISearchCatalogManager::GetItemsChangedSink
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
 - ISearchCatalogManager.GetItemsChangedSink
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
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



