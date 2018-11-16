---
UID: NF:searchapi.ISearchItemsChangedSink.StartedMonitoringScope
title: ISearchItemsChangedSink::StartedMonitoringScope
author: windows-sdk-content
description: Permits an index-managed notification source to add itself to a list of &#0034;monitored scopes&#0034;.
old-location: search\_search_ISearchItemsChangedSink_StartedMonitoringScope.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\notifications\isearchitemschangedsink\startedmonitoringscope.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: ISearchItemsChangedSink interface [search],StartedMonitoringScope method, ISearchItemsChangedSink.StartedMonitoringScope, ISearchItemsChangedSink::StartedMonitoringScope, StartedMonitoringScope, StartedMonitoringScope method [search], StartedMonitoringScope method [search],ISearchItemsChangedSink interface, _search_ISearchItemsChangedSink_StartedMonitoringScope, search._search_ISearchItemsChangedSink_StartedMonitoringScope, searchapi/ISearchItemsChangedSink::StartedMonitoringScope
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - ISearchItemsChangedSink.StartedMonitoringScope
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
- apiref
: 
- COM
: 
- searchapi.h
: 
- ISearchItemsChangedSink.StartedMonitoringScope
: 
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



When a notification agent comes online it calls <a href="https://msdn.microsoft.com/en-us/library/Bb231456(v=VS.85).aspx">StartedMonitoringScope</a> which adds the scope to the list of sources. If the source is new (removed previously by <a href="https://msdn.microsoft.com/en-us/library/Bb231457(v=VS.85).aspx">StoppedMonitoringScope</a>, or never created in the first place) the indexer starts an incremental crawl of the corresponding document store. This is designed to pick up any changes in the store that occurred while the notification agent was offline. 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/Bb266492(v=VS.85).aspx">ISearchCrawlScopeManager</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb231461(v=VS.85).aspx">ISearchItemsChangedSink</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb266457(v=VS.85).aspx">ISearchScopeRule</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb266528(v=VS.85).aspx">Notifying the Index of Changes</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/Bb231464(v=VS.85).aspx">StoppedMonitoringScope</a>
 

 

