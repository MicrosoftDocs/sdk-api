---
UID: NF:searchapi.ISearchCatalogManager.RegisterViewForNotification
title: ISearchCatalogManager::RegisterViewForNotification
author: windows-sdk-content
description: Not implemented.
old-location: search\_search_ISearchCatalogManager_RegisterViewForNotification.htm
old-project: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\indexmanagement\isearchcatalogmanager\registerviewfornotification.htm
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: ISearchCatalogManager interface [search],RegisterViewForNotification method, ISearchCatalogManager.RegisterViewForNotification, ISearchCatalogManager::RegisterViewForNotification, RegisterViewForNotification, RegisterViewForNotification method [search], RegisterViewForNotification method [search],ISearchCatalogManager interface, _search_ISearchCatalogManager_RegisterViewForNotification, search._search_ISearchCatalogManager_RegisterViewForNotification, searchapi/ISearchCatalogManager::RegisterViewForNotification
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: searchapi.h
req.include-header: Searchapi.h
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
 - searchapi.h
api_name:
 - ISearchCatalogManager.RegisterViewForNotification
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# ISearchCatalogManager::RegisterViewForNotification


## -description


Not implemented.


## -parameters




### -param pszView [in]

Type: <b>LPCWSTR</b>

A pointer to the name of the view.


### -param pViewChangedSink [in]

Type: <b><a href="https://msdn.microsoft.com/library/Bb231452(v=VS.85).aspx">ISearchViewChangedSink</a>*</b>

Pointer to the <a href="https://msdn.microsoft.com/library/Bb231452(v=VS.85).aspx">ISearchViewChangedSink</a> object to receive notifications.


### -param pdwCookie [out]

Type: <b>DWORD*</b>


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



