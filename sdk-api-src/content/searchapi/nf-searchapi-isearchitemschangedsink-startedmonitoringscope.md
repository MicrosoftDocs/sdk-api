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

# ISearchItemsChangedSink::StartedMonitoringScope


## -description


Permits an index-managed notification source to add itself to a list of "monitored scopes".


## -parameters




### -param pszURL [in]

Type: <b>LPCWSTR</b>

A pointer to a null-terminated, Unicode string that is the start address for the scope of monitoring.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



When a notification agent comes online it calls <a href="https://msdn.microsoft.com/97143616-05ed-4693-9a83-25ced1d6de07">StartedMonitoringScope</a> which adds the scope to the list of sources. If the source is new (removed previously by <a href="https://msdn.microsoft.com/18c01b84-4b31-4bf0-a48f-ede68aad604d">StoppedMonitoringScope</a>, or never created in the first place) the indexer starts an incremental crawl of the corresponding document store. This is designed to pick up any changes in the store that occurred while the notification agent was offline. 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/8b731941-f1f6-402e-8cee-3c493e3c369d">ISearchCrawlScopeManager</a>



<a href="https://msdn.microsoft.com/7ad55cf5-5024-4a30-a465-536fb1429b19">ISearchItemsChangedSink</a>



<a href="https://msdn.microsoft.com/ace8d4f8-ffe0-45ff-8ba4-691efad23013">ISearchScopeRule</a>



<a href="https://msdn.microsoft.com/817550e2-a256-48d5-9fa6-1ea04f8b8589">Notifying the Index of Changes</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/5088bd59-115d-482c-b3cf-d6a38ff95287">StoppedMonitoringScope</a>
 

 

