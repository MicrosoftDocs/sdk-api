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

# ISearchPersistentItemsChangedSink::StartedMonitoringScope


## -description


Called by a notifications provider to notify the indexer to monitor changes to items within a specified hierarchical scope.


## -parameters




### -param pszURL [in]

Type: <b>LPCWSTR</b>

Pointer to a null-terminated Unicode string that is the start address for the scope to be monitored.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



When notification loss occurs, a notification agent comes online and calls <a href="https://msdn.microsoft.com/6baf05fd-a487-4e42-a054-c7058188454b">StartedMonitoringScope</a>, which permits an index-managed notification source to add itself to a list of "monitored scopes". The indexer starts an incremental crawl of the corresponding document store. The indexer crawls these scopes incrementally until the extreme conditions that caused the loss of notifications are no longer present. This method ensures that any changes in the store that occur during a period of notification loss are detected.

Under normal circumstances, the list of monitored scopes is not used. Notification loss is rare, and usually occurs only when disk space is extremely low.



