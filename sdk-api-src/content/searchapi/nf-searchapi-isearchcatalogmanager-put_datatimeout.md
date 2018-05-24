---
UID: NF:searchapi.ISearchCatalogManager.put_DataTimeout
title: ISearchCatalogManager::put_DataTimeout
author: windows-driver-content
description: Sets the time-out value for data transactions between the indexer and the search filter host. This information is stored in the TIMEOUT_INFO structure and is measured in seconds.
old-location: search\_search_ISearchCatalogManager_put_DataTimeout.htm
old-project: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\indexmanagement\isearchcatalogmanager\put_datatimeout.htm
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: ISearchCatalogManager interface [search],put_DataTimeout method, ISearchCatalogManager.put_DataTimeout, ISearchCatalogManager::put_DataTimeout, _search_ISearchCatalogManager_put_DataTimeout, put_DataTimeout, put_DataTimeout method [search], put_DataTimeout method [search],ISearchCatalogManager interface, search._search_ISearchCatalogManager_put_DataTimeout, searchapi/ISearchCatalogManager::put_DataTimeout
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
-	ISearchCatalogManager.put_DataTimeout
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# ISearchCatalogManager::put_DataTimeout


## -description


Sets the time-out value for data transactions between the indexer and the search filter host. This information is stored in the <a href="https://msdn.microsoft.com/f6032470-abfd-4808-921c-7fa687ed640f">TIMEOUT_INFO</a> structure and is measured in seconds.


## -parameters




### -param dwDataTimeout [in]

Type: <b>DWORD</b>

The number of seconds that the indexer will wait between chunks of data.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The indexer expects the first chunk of the document to be received within the connection time-out interval and any subsequent chunks to be received within the data time-out interval. These time-out values help prevent filters and protocol handlers from  failing or causing performance issues.
            



