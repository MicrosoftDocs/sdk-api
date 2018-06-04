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

# ISearchPersistentItemsChangedSink::OnItemsChanged


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



