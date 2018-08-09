---
UID: NF:searchapi.ISearchCatalogManager.GetParameter
title: ISearchCatalogManager::GetParameter
author: windows-sdk-content
description: Not implemented.
old-location: search\_search_ISearchCatalogManager_GetParameter.htm
old-project: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\indexmanagement\isearchcatalogmanager\getparameter.htm
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: GetParameter, GetParameter method [search], GetParameter method [search],ISearchCatalogManager interface, ISearchCatalogManager interface [search],GetParameter method, ISearchCatalogManager.GetParameter, ISearchCatalogManager::GetParameter, _search_ISearchCatalogManager_GetParameter, search._search_ISearchCatalogManager_GetParameter, searchapi/ISearchCatalogManager::GetParameter
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
 - ISearchCatalogManager.GetParameter
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# ISearchCatalogManager::GetParameter


## -description


Not implemented.


## -parameters




### -param pszName [in]

Type: <b>LPCWSTR</b>

The name of the parameter to be retrieved.
                


### -param ppValue [out, retval]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa380072(v=VS.85).aspx">PROPVARIANT</a>**</b>

Receives a pointer to the value of the parameter. 
                


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



