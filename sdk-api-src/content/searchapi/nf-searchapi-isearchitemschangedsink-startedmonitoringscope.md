---
UID: NF:searchapi.ISearchItemsChangedSink.StartedMonitoringScope
title: ISearchItemsChangedSink::StartedMonitoringScope
author: windows-sdk-content
description: Permits an index-managed notification source to add itself to a list of &#0034;monitored scopes&#0034;.
old-location: search\_search_ISearchItemsChangedSink_StartedMonitoringScope.htm
old-project: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\notifications\isearchitemschangedsink\startedmonitoringscope.htm
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: ISearchItemsChangedSink interface [search],StartedMonitoringScope method, ISearchItemsChangedSink.StartedMonitoringScope, ISearchItemsChangedSink::StartedMonitoringScope, StartedMonitoringScope, StartedMonitoringScope method [search], StartedMonitoringScope method [search],ISearchItemsChangedSink interface, _search_ISearchItemsChangedSink_StartedMonitoringScope, search._search_ISearchItemsChangedSink_StartedMonitoringScope, searchapi/ISearchItemsChangedSink::StartedMonitoringScope
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: searchapi.h
req.include-header: 
req.redist: Windows Desktop Search (WDS) 3.0
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
tech.root: 
req.typenames: ROWSETEVENT_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Searchapi.h
api_name:
 - ISearchItemsChangedSink.StartedMonitoringScope
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
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
 

 

