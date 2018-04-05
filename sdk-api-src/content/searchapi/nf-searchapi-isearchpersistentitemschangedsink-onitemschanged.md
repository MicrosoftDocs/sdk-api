---
UID: NF:searchapi.ISearchPersistentItemsChangedSink.OnItemsChanged
title: ISearchPersistentItemsChangedSink::OnItemsChanged method
author: windows-driver-content
description: Notifies the indexer to index changed items.
old-location: search\_search_ISearchPersistentItemsChangedSink_OnItemsChanged.htm
old-project: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\notifications\isearchpersistentitemschangedsink\onitemschanged.htm
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: ISearchPersistentItemsChangedSink, ISearchPersistentItemsChangedSink interface [search], OnItemsChanged method, ISearchPersistentItemsChangedSink::OnItemsChanged, OnItemsChanged method [search], OnItemsChanged method [search], ISearchPersistentItemsChangedSink interface, OnItemsChanged,ISearchPersistentItemsChangedSink.OnItemsChanged, _search_ISearchPersistentItemsChangedSink_OnItemsChanged, search._search_ISearchPersistentItemsChangedSink_OnItemsChanged, searchapi/ISearchPersistentItemsChangedSink::OnItemsChanged
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: searchapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Searchnotifications.idl
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
-	ISearchPersistentItemsChangedSink.OnItemsChanged
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# ISearchPersistentItemsChangedSink::OnItemsChanged method


## -description



            Notifies the indexer to index changed items.
        


## -parameters




### -param dwNumberOfChanges [in]

Type: <b>DWORD</b>


                    The number of changes being reported.
                


### -param DataChangeEntries [in]

Type: <b><a href="https://msdn.microsoft.com/33b131fb-3565-4625-a6a9-6c7b4aef6860">SEARCH_ITEM_PERSISTENT_CHANGE</a>[]</b>


                    An array of structures of type <a href="https://msdn.microsoft.com/33b131fb-3565-4625-a6a9-6c7b4aef6860">SEARCH_ITEM_PERSISTENT_CHANGE</a> identifying the details for each change.
                


### -param hrCompletionCodes [out]

Type: <b>HRESULT[]</b>


                    Indicates whether each URL was accepted for indexing.
                


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



