---
UID: NF:searchapi.ISearchPersistentItemsChangedSink.StartedMonitoringScope
title: ISearchPersistentItemsChangedSink::StartedMonitoringScope (searchapi.h)
description: Called by a notifications provider to notify the indexer to monitor changes to items within a specified hierarchical scope.
helpviewer_keywords: ["ISearchPersistentItemsChangedSink interface [search]","StartedMonitoringScope method","ISearchPersistentItemsChangedSink.StartedMonitoringScope","ISearchPersistentItemsChangedSink::StartedMonitoringScope","StartedMonitoringScope","StartedMonitoringScope method [search]","StartedMonitoringScope method [search]","ISearchPersistentItemsChangedSink interface","_search_ISearchPersistentItemsChangedSink_StartedMonitoringScope","search._search_ISearchPersistentItemsChangedSink_StartedMonitoringScope","searchapi/ISearchPersistentItemsChangedSink::StartedMonitoringScope"]
old-location: search\_search_ISearchPersistentItemsChangedSink_StartedMonitoringScope.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\notifications\isearchpersistentitemschangedsink\startedmonitoringscope.htm
ms.date: 12/05/2018
ms.keywords: ISearchPersistentItemsChangedSink interface [search],StartedMonitoringScope method, ISearchPersistentItemsChangedSink.StartedMonitoringScope, ISearchPersistentItemsChangedSink::StartedMonitoringScope, StartedMonitoringScope, StartedMonitoringScope method [search], StartedMonitoringScope method [search],ISearchPersistentItemsChangedSink interface, _search_ISearchPersistentItemsChangedSink_StartedMonitoringScope, search._search_ISearchPersistentItemsChangedSink_StartedMonitoringScope, searchapi/ISearchPersistentItemsChangedSink::StartedMonitoringScope
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
f1_keywords:
 - ISearchPersistentItemsChangedSink::StartedMonitoringScope
 - searchapi/ISearchPersistentItemsChangedSink::StartedMonitoringScope
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Searchapi.h
api_name:
 - ISearchPersistentItemsChangedSink.StartedMonitoringScope
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

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

When notification loss occurs, a notification agent comes online and calls <a href="/windows/desktop/api/searchapi/nf-searchapi-isearchitemschangedsink-startedmonitoringscope">StartedMonitoringScope</a>, which permits an index-managed notification source to add itself to a list of "monitored scopes". The indexer starts an incremental crawl of the corresponding document store. The indexer crawls these scopes incrementally until the extreme conditions that caused the loss of notifications are no longer present. This method ensures that any changes in the store that occur during a period of notification loss are detected.

Under normal circumstances, the list of monitored scopes is not used. Notification loss is rare, and usually occurs only when disk space is extremely low.