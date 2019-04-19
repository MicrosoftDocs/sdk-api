---
UID: NF:searchapi.ISearchItemsChangedSink.OnItemsChanged
title: ISearchItemsChangedSink::OnItemsChanged (searchapi.h)
author: windows-sdk-content
description: Call this method to notify an indexer to re-index some changed items.
old-location: search\_search_ISearchItemsChangedSink_OnItemsChanged.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\notifications\isearchitemschangedsink\onitemschanged.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ISearchItemsChangedSink interface [search],OnItemsChanged method, ISearchItemsChangedSink.OnItemsChanged, ISearchItemsChangedSink::OnItemsChanged, OnItemsChanged, OnItemsChanged method [search], OnItemsChanged method [search],ISearchItemsChangedSink interface, _search_ISearchItemsChangedSink_OnItemsChanged, search._search_ISearchItemsChangedSink_OnItemsChanged, searchapi/ISearchItemsChangedSink::OnItemsChanged
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
req.idl: 
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
 - ISearchItemsChangedSink.OnItemsChanged
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
---

# ISearchItemsChangedSink::OnItemsChanged


## -description


   
            Call this method to notify an indexer to re-index some changed items.
        


## -parameters




### -param dwNumberOfChanges [in]

Type: <b>DWORD</b>

The number of items that have changed.
                


### -param rgDataChangeEntries [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa965371(v=VS.85).aspx">SEARCH_ITEM_CHANGE</a>[]</b>

An array of <a href="https://msdn.microsoft.com/en-us/library/Aa965371(v=VS.85).aspx">SEARCH_ITEM_CHANGE</a> structures, describing the type of changes to and the paths or URLs of each item.
                


### -param rgdwDocIds [out]

Type: <b>DWORD[]</b>

Receives a pointer to an array of document identifiers for the items that changed. 
                


### -param rghrCompletionCodes [out]

Type: <b>HRESULT[]</b>

Receives a pointer to an array of completion codes for <i>rgdwDocIds</i> indicating whether each item was accepted for indexing. 
                


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



When there are multiple change notifications, the <b>priority</b> member of the <a href="https://msdn.microsoft.com/en-us/library/Aa965371(v=VS.85).aspx">SEARCH_ITEM_CHANGE</a> structure indicates the priority of processing.
            




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb231461(v=VS.85).aspx">ISearchItemsChangedSink</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb266528(v=VS.85).aspx">Notifying the Index of Changes</a>
 

 

