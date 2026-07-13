---
UID: NF:searchapi.ISearchItemsChangedSink.StartedMonitoringScope
title: ISearchItemsChangedSink::StartedMonitoringScope (searchapi.h)
description: Permits an index-managed notification source to add itself to a list of &quot;monitored scopes&quot;.
helpviewer_keywords: ["ISearchItemsChangedSink interface [search]","StartedMonitoringScope method","ISearchItemsChangedSink.StartedMonitoringScope","ISearchItemsChangedSink::StartedMonitoringScope","StartedMonitoringScope","StartedMonitoringScope method [search]","StartedMonitoringScope method [search]","ISearchItemsChangedSink interface","_search_ISearchItemsChangedSink_StartedMonitoringScope","search._search_ISearchItemsChangedSink_StartedMonitoringScope","searchapi/ISearchItemsChangedSink::StartedMonitoringScope"]
old-location: search\_search_ISearchItemsChangedSink_StartedMonitoringScope.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\notifications\isearchitemschangedsink\startedmonitoringscope.htm
ms.date: 12/05/2018
ms.keywords: ISearchItemsChangedSink interface [search],StartedMonitoringScope method, ISearchItemsChangedSink.StartedMonitoringScope, ISearchItemsChangedSink::StartedMonitoringScope, StartedMonitoringScope, StartedMonitoringScope method [search], StartedMonitoringScope method [search],ISearchItemsChangedSink interface, _search_ISearchItemsChangedSink_StartedMonitoringScope, search._search_ISearchItemsChangedSink_StartedMonitoringScope, searchapi/ISearchItemsChangedSink::StartedMonitoringScope
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
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
f1_keywords:
 - ISearchItemsChangedSink::StartedMonitoringScope
 - searchapi/ISearchItemsChangedSink::StartedMonitoringScope
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
 - ISearchItemsChangedSink.StartedMonitoringScope
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

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

When a notification agent comes online it calls <a href="/windows/desktop/api/searchapi/nf-searchapi-isearchpersistentitemschangedsink-startedmonitoringscope">StartedMonitoringScope</a> which adds the scope to the list of sources. If the source is new (removed previously by <a href="/windows/desktop/api/searchapi/nf-searchapi-isearchpersistentitemschangedsink-stoppedmonitoringscope">StoppedMonitoringScope</a>, or never created in the first place) the indexer starts an incremental crawl of the corresponding document store. This is designed to pick up any changes in the store that occurred while the notification agent was offline.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/searchapi/nn-searchapi-isearchcrawlscopemanager">ISearchCrawlScopeManager</a>



<a href="/windows/desktop/api/searchapi/nn-searchapi-isearchitemschangedsink">ISearchItemsChangedSink</a>



<a href="/windows/desktop/api/searchapi/nn-searchapi-isearchscoperule">ISearchScopeRule</a>



<a href="/windows/desktop/search/-search-3x-wds-notifyingofchanges">Notifying the Index of Changes</a>



<b>Reference</b>



<a href="/windows/desktop/api/searchapi/nf-searchapi-isearchitemschangedsink-stoppedmonitoringscope">StoppedMonitoringScope</a>