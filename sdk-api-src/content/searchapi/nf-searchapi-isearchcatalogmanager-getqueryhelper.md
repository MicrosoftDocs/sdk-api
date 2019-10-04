---
UID: NF:searchapi.ISearchCatalogManager.GetQueryHelper
title: ISearchCatalogManager::GetQueryHelper (searchapi.h)
author: windows-sdk-content
description: Gets the ISearchQueryHelper interface for the current catalog.
old-location: search\_search_ISearchCatalogManager_GetQueryHelper.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\indexmanagement\isearchcatalogmanager\getqueryhelper.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetQueryHelper, GetQueryHelper method [search], GetQueryHelper method [search],ISearchCatalogManager interface, ISearchCatalogManager interface [search],GetQueryHelper method, ISearchCatalogManager.GetQueryHelper, ISearchCatalogManager::GetQueryHelper, _search_ISearchCatalogManager_GetQueryHelper, search._search_ISearchCatalogManager_GetQueryHelper, searchapi/ISearchCatalogManager::GetQueryHelper
ms.topic: method
f1_keywords: 
 - "searchapi/ISearchCatalogManager.GetQueryHelper"
dev_langs:
 - c++
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
 - ISearchCatalogManager.GetQueryHelper
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
---

# ISearchCatalogManager::GetQueryHelper


## -description


Gets the <a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nn-searchapi-isearchqueryhelper">ISearchQueryHelper</a> interface for the current catalog.
        


## -parameters




### -param ppSearchQueryHelper [out, retval]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nn-searchapi-isearchqueryhelper">ISearchQueryHelper</a>**</b>

Receives the address of a pointer to a new instance of the <a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nn-searchapi-isearchqueryhelper">ISearchQueryHelper</a> interface with default settings.
                


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



After the <a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nn-searchapi-isearchqueryhelper">ISearchQueryHelper</a> interface is created, use the put... methods for this interface to change settings. Settings for the <b>ISearchQueryHelper</b> object are relevant only until the settings are changed again or the item is released. When the item is next created, settings are set to default values.



