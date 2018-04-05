---
UID: NF:searchapi.ISearchCatalogManager.SetParameter
title: ISearchCatalogManager::SetParameter method
author: windows-driver-content
description: Sets a name/value parameter for the catalog.
old-location: search\_search_ISearchCatalogManager_SetParameter.htm
old-project: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\indexmanagement\isearchcatalogmanager\setparameter.htm
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: ISearchCatalogManager, ISearchCatalogManager interface [search], SetParameter method, ISearchCatalogManager::SetParameter, SetParameter method [search], SetParameter method [search], ISearchCatalogManager interface, SetParameter,ISearchCatalogManager.SetParameter, _search_ISearchCatalogManager_SetParameter, search._search_ISearchCatalogManager_SetParameter, searchapi/ISearchCatalogManager::SetParameter
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
-	ISearchCatalogManager.SetParameter
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# ISearchCatalogManager::SetParameter method


## -description



            Sets a name/value parameter for the catalog.
        


## -parameters




### -param pszName [in]

Type: <b>LPCWSTR</b>


                    The name of the parameter to change.
                


### -param pValue [in]

Type: <b><a href="_stg_propvariant">PROPVARIANT</a>*</b>


                    A pointer to the new value for the parameter.
                


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



