---
UID: NF:searchapi.ISearchCatalogManager.get_ConnectTimeout
title: ISearchCatalogManager::get_ConnectTimeout (searchapi.h)
author: windows-sdk-content
description: Gets the connection time-out value for connecting to a store for indexing.
old-location: search\_search_ISearchCatalogManager_get_ConnectTimeout.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\indexmanagement\isearchcatalogmanager\get_connecttimeout.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ISearchCatalogManager interface [search],get_ConnectTimeout method, ISearchCatalogManager.get_ConnectTimeout, ISearchCatalogManager::get_ConnectTimeout, _search_ISearchCatalogManager_get_ConnectTimeout, get_ConnectTimeout, get_ConnectTimeout method [search], get_ConnectTimeout method [search],ISearchCatalogManager interface, search._search_ISearchCatalogManager_get_ConnectTimeout, searchapi/ISearchCatalogManager::get_ConnectTimeout
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
 - ISearchCatalogManager.get_ConnectTimeout
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
---

# ISearchCatalogManager::get_ConnectTimeout


## -description


Gets the connection time-out value for connecting to a store for indexing.


## -parameters




### -param pdwConnectTimeout [out, retval]

Type: <b>DWORD*</b>

Receives a pointer to the time-out value, in seconds, from the <a href="https://msdn.microsoft.com/en-us/library/Aa965374(v=VS.85).aspx">TIMEOUT_INFO</a> structure.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The indexer expects the first chunk of the document to be received within the connection time-out interval and any subsequent chunks to be received within the data time-out interval. These time-out values help prevent filters and protocol handlers from  failing or causing performance issues.
            



