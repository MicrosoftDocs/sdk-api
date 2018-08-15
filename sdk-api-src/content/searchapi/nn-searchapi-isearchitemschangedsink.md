---
UID: NN:searchapi.ISearchItemsChangedSink
title: ISearchItemsChangedSink
author: windows-sdk-content
description: Provides notifications for changes to indexed items. Also provides notification of the hierarchical scope that is being monitored for changed items.
old-location: search\_search_ISearchItemsChangedSink.htm
old-project: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\notifications\isearchitemschangedsink\isearchitemschangedsink.htm
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: ISearchItemsChangedSink, ISearchItemsChangedSink interface [search], ISearchItemsChangedSink interface [search],described, _search_ISearchItemsChangedSink, search._search_ISearchItemsChangedSink, searchapi/ISearchItemsChangedSink
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
 - ISearchItemsChangedSink
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# ISearchItemsChangedSink interface


## -description


Provides notifications for changes to indexed items. Also provides notification of the hierarchical scope that is being monitored for changed items.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISearchItemsChangedSink</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ISearchItemsChangedSink</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISearchItemsChangedSink</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb231462(v=VS.85).aspx">OnItemsChanged</a>
</td>
<td align="left" width="63%">
   
            Call this method to notify an indexer to re-index some changed items.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb231463(v=VS.85).aspx">StartedMonitoringScope</a>
</td>
<td align="left" width="63%">
Permits an index-managed notification source to add itself to a list of "monitored scopes".

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb231464(v=VS.85).aspx">StoppedMonitoringScope</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb266528(v=VS.85).aspx">Notifying the Index of Changes</a>
 

 

