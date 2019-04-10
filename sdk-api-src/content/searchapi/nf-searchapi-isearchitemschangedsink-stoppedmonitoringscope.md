---
UID: NF:searchapi.ISearchItemsChangedSink.StoppedMonitoringScope
title: ISearchItemsChangedSink::StoppedMonitoringScope (searchapi.h)
author: windows-sdk-content
description: Not implemented.
old-location: search\_search_ISearchItemsChangedSink_StoppedMonitoringScope.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\notifications\isearchitemschangedsink\stoppedmonitoringscope.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ISearchItemsChangedSink interface [search],StoppedMonitoringScope method, ISearchItemsChangedSink.StoppedMonitoringScope, ISearchItemsChangedSink::StoppedMonitoringScope, StoppedMonitoringScope, StoppedMonitoringScope method [search], StoppedMonitoringScope method [search],ISearchItemsChangedSink interface, _search_ISearchItemsChangedSink_StoppedMonitoringScope, search._search_ISearchItemsChangedSink_StoppedMonitoringScope, searchapi/ISearchItemsChangedSink::StoppedMonitoringScope
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - searchapi.h
api_name:
 - ISearchItemsChangedSink.StoppedMonitoringScope
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
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

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/Bb266492(v=VS.85).aspx">ISearchCrawlScopeManager</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb231461(v=VS.85).aspx">ISearchItemsChangedSink</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb266457(v=VS.85).aspx">ISearchScopeRule</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb266528(v=VS.85).aspx">Notifying the Index of Changes</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/Bb231463(v=VS.85).aspx">StartedMonitoringScope</a>
 

 

