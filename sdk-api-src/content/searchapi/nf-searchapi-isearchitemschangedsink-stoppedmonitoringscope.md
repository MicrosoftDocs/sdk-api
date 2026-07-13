---
UID: NF:searchapi.ISearchItemsChangedSink.StoppedMonitoringScope
title: ISearchItemsChangedSink::StoppedMonitoringScope (searchapi.h)
description: Not implemented. (ISearchItemsChangedSink.StoppedMonitoringScope)
helpviewer_keywords: ["ISearchItemsChangedSink interface [search]","StoppedMonitoringScope method","ISearchItemsChangedSink.StoppedMonitoringScope","ISearchItemsChangedSink::StoppedMonitoringScope","StoppedMonitoringScope","StoppedMonitoringScope method [search]","StoppedMonitoringScope method [search]","ISearchItemsChangedSink interface","_search_ISearchItemsChangedSink_StoppedMonitoringScope","search._search_ISearchItemsChangedSink_StoppedMonitoringScope","searchapi/ISearchItemsChangedSink::StoppedMonitoringScope"]
old-location: search\_search_ISearchItemsChangedSink_StoppedMonitoringScope.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\notifications\isearchitemschangedsink\stoppedmonitoringscope.htm
ms.date: 12/05/2018
ms.keywords: ISearchItemsChangedSink interface [search],StoppedMonitoringScope method, ISearchItemsChangedSink.StoppedMonitoringScope, ISearchItemsChangedSink::StoppedMonitoringScope, StoppedMonitoringScope, StoppedMonitoringScope method [search], StoppedMonitoringScope method [search],ISearchItemsChangedSink interface, _search_ISearchItemsChangedSink_StoppedMonitoringScope, search._search_ISearchItemsChangedSink_StoppedMonitoringScope, searchapi/ISearchItemsChangedSink::StoppedMonitoringScope
req.header: searchapi.h
req.include-header: Searchapi.h
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
 - ISearchItemsChangedSink::StoppedMonitoringScope
 - searchapi/ISearchItemsChangedSink::StoppedMonitoringScope
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - searchapi.h
api_name:
 - ISearchItemsChangedSink.StoppedMonitoringScope
---

# ISearchItemsChangedSink::StoppedMonitoringScope


## -description

Not implemented.

## -parameters

### -param pszURL [in]

Type: <b>LPCWSTR</b>

The pointer to a null-terminated, Unicode string containing the start address for the scope of monitoring.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/searchapi/nn-searchapi-isearchcrawlscopemanager">ISearchCrawlScopeManager</a>



<a href="/windows/desktop/api/searchapi/nn-searchapi-isearchitemschangedsink">ISearchItemsChangedSink</a>



<a href="/windows/desktop/api/searchapi/nn-searchapi-isearchscoperule">ISearchScopeRule</a>



<a href="/windows/desktop/search/-search-3x-wds-notifyingofchanges">Notifying the Index of Changes</a>



<b>Reference</b>



<a href="/windows/desktop/api/searchapi/nf-searchapi-isearchitemschangedsink-startedmonitoringscope">StartedMonitoringScope</a>
