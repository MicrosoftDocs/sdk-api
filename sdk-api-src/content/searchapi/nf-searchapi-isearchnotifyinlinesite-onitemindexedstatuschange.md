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

# ISearchNotifyInlineSite::OnItemIndexedStatusChange


## -description



            Called by the search service to notify the client when the status of a particular document or item changes.
        


## -parameters




### -param sipStatus [in]

Type: <b><a href="https://msdn.microsoft.com/fdd80abf-7362-45ca-96da-19824eb8d650">SEARCH_INDEXING_PHASE</a></b>


                    The <a href="https://msdn.microsoft.com/fdd80abf-7362-45ca-96da-19824eb8d650">SEARCH_INDEXING_PHASE</a> status of each document in the array being sent.
                


### -param dwNumEntries [in]

Type: <b>DWORD</b>


                    The number of entries in <i>rgItemStatusEntries</i>.
                


### -param rgItemStatusEntries [in]

Type: <b><a href="https://msdn.microsoft.com/c62790bf-1c96-4566-afcc-c03810677dfb">SEARCH_ITEM_INDEXING_STATUS</a>[]</b>


                    An array of <a href="https://msdn.microsoft.com/c62790bf-1c96-4566-afcc-c03810677dfb">SEARCH_ITEM_INDEXING_STATUS</a> structures containing status update information.
                


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/5837ccf6-1156-44a5-9135-3e3b47244f9d">ISearchNotifyInlineSite</a>



<a href="https://msdn.microsoft.com/817550e2-a256-48d5-9fa6-1ea04f8b8589">Notifying the Index of Changes</a>
 

 

