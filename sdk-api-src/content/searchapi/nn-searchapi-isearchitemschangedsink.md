---
UID: NN:searchapi.ISearchItemsChangedSink
title: ISearchItemsChangedSink
author: windows-driver-content
description: Provides notifications for changes to indexed items. Also provides notification of the hierarchical scope that is being monitored for changed items.
old-location: search\_search_ISearchItemsChangedSink.htm
old-project: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\notifications\isearchitemschangedsink\isearchitemschangedsink.htm
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: ISearchItemsChangedSink, ISearchItemsChangedSink interface [search], ISearchItemsChangedSink interface [search],described, _search_ISearchItemsChangedSink, search._search_ISearchItemsChangedSink, searchapi/ISearchItemsChangedSink
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
req.typenames: ROWSETEVENT_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Searchapi.h
api_name:
-	ISearchItemsChangedSink
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
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
<a href="https://msdn.microsoft.com/3f31ab2c-f788-4b22-9706-dbfcd3bfa3ae">OnItemsChanged</a>
</td>
<td align="left" width="63%">
   
            Call this method to notify an indexer to re-index some changed items.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6baf05fd-a487-4e42-a054-c7058188454b">StartedMonitoringScope</a>
</td>
<td align="left" width="63%">
Permits an index-managed notification source to add itself to a list of "monitored scopes".

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5088bd59-115d-482c-b3cf-d6a38ff95287">StoppedMonitoringScope</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/817550e2-a256-48d5-9fa6-1ea04f8b8589">Notifying the Index of Changes</a>
 

 

