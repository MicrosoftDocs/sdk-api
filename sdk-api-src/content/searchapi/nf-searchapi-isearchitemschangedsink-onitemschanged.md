---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# ISearchItemsChangedSink::OnItemsChanged


## -description


   
            Call this method to notify an indexer to re-index some changed items.
        


## -parameters




### -param dwNumberOfChanges [in]

Type: <b>DWORD</b>

The number of items that have changed.
                


### -param rgDataChangeEntries [in]

Type: <b><a href="https://msdn.microsoft.com/83ed1c76-7210-4d0b-a6e2-461bc331e168">SEARCH_ITEM_CHANGE</a>[]</b>


                    An array of <a href="https://msdn.microsoft.com/83ed1c76-7210-4d0b-a6e2-461bc331e168">SEARCH_ITEM_CHANGE</a> structures, describing the type of changes to and the paths or URLs of each item.
                


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




                When there are multiple change notifications, the <b>priority</b> member of the <a href="https://msdn.microsoft.com/83ed1c76-7210-4d0b-a6e2-461bc331e168">SEARCH_ITEM_CHANGE</a> structure indicates the priority of processing.
            




## -see-also




<a href="https://msdn.microsoft.com/7ad55cf5-5024-4a30-a465-536fb1429b19">ISearchItemsChangedSink</a>



<a href="https://msdn.microsoft.com/817550e2-a256-48d5-9fa6-1ea04f8b8589">Notifying the Index of Changes</a>
 

 

