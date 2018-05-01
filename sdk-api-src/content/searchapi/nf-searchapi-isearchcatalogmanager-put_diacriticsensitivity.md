---
UID: NF:searchapi.ISearchCatalogManager.put_DiacriticSensitivity
title: ISearchCatalogManager::put_DiacriticSensitivity method
author: windows-driver-content
description: Sets a value that determines whether the catalog is sensitive to diacritics. A diacritic is a mark added to a letter to indicate a special phonetic value or pronunciation.
old-location: search\_search_ISearchCatalogManager_put_DiacriticSensitivity.htm
old-project: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\indexmanagement\isearchcatalogmanager\put_diacriticsensitivity.htm
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: ISearchCatalogManager, ISearchCatalogManager interface [search], put_DiacriticSensitivity method, ISearchCatalogManager::put_DiacriticSensitivity, _search_ISearchCatalogManager_put_DiacriticSensitivity, put_DiacriticSensitivity method [search], put_DiacriticSensitivity method [search], ISearchCatalogManager interface, put_DiacriticSensitivity,ISearchCatalogManager.put_DiacriticSensitivity, search._search_ISearchCatalogManager_put_DiacriticSensitivity, searchapi/ISearchCatalogManager::put_DiacriticSensitivity
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
-	ISearchCatalogManager.put_DiacriticSensitivity
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# ISearchCatalogManager::put_DiacriticSensitivity method


## -description


Sets a value that determines whether the catalog is sensitive to diacritics. A diacritic is a mark added to a letter to indicate a special phonetic value or pronunciation.


## -parameters




### -param fDiacriticSensitive [in]

Type: <b>BOOL</b>

A Boolean value that determines whether the catalog is sensitive to diacritics. <b>TRUE</b> if the catalog is sensitive to and recognizes diacritics; otherwise, <b>FALSE</b>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



