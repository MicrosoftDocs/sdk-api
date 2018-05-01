---
UID: NF:searchapi.ISearchCatalogManager.GetPersistentItemsChangedSink
title: ISearchCatalogManager::GetPersistentItemsChangedSink method
author: windows-driver-content
description: Gets the change notification event sink interface for a client. This method is used by client applications and protocol handlers to notify the indexer of changes.
old-location: search\_search_ISearchCatalogManager_GetPersistentItemsChangedSink.htm
old-project: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\indexmanagement\isearchcatalogmanager\getpersistentitemschangedsink.htm
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: GetPersistentItemsChangedSink method [search], GetPersistentItemsChangedSink method [search], ISearchCatalogManager interface, GetPersistentItemsChangedSink,ISearchCatalogManager.GetPersistentItemsChangedSink, ISearchCatalogManager, ISearchCatalogManager interface [search], GetPersistentItemsChangedSink method, ISearchCatalogManager::GetPersistentItemsChangedSink, _search_ISearchCatalogManager_GetPersistentItemsChangedSink, search._search_ISearchCatalogManager_GetPersistentItemsChangedSink, searchapi/ISearchCatalogManager::GetPersistentItemsChangedSink
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
-	ISearchCatalogManager.GetPersistentItemsChangedSink
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# ISearchCatalogManager::GetPersistentItemsChangedSink method


## -description


Gets the change notification event sink interface for a client. This method is used by client applications and protocol handlers to notify the indexer of changes.


## -parameters




### -param ppISearchPersistentItemsChangedSink [out, retval]

Type: <b><a href="https://msdn.microsoft.com/ce2a5b93-c8df-4acb-9b26-7ff1004124af">ISearchPersistentItemsChangedSink</a>**</b>


                    Receives the address of a pointer to a new <a href="https://msdn.microsoft.com/ce2a5b93-c8df-4acb-9b26-7ff1004124af">ISearchPersistentItemsChangedSink</a> interface for this catalog.
                


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



