---
UID: NN:searchapi.ISearchPersistentItemsChangedSink
title: ISearchPersistentItemsChangedSink
author: windows-sdk-content
description: Provides methods for passing change notifications to alert the indexer that items need to be updated.
old-location: search\_search_ISearchPersistentItemsChangedSink.htm
old-project: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\notifications\isearchpersistentitemschangedsink\isearchpersistentitemschangedsink.htm
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: ISearchPersistentItemsChangedSink, ISearchPersistentItemsChangedSink interface [search], ISearchPersistentItemsChangedSink interface [search],described, _search_ISearchPersistentItemsChangedSink, search._search_ISearchPersistentItemsChangedSink, searchapi/ISearchPersistentItemsChangedSink
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
 - ISearchPersistentItemsChangedSink
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# ISearchPersistentItemsChangedSink interface


## -description


Provides methods for passing change notifications to alert the indexer that items need to be updated.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISearchPersistentItemsChangedSink</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ISearchPersistentItemsChangedSink</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISearchPersistentItemsChangedSink</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/975f687f-65c7-4086-b99c-c1b1419a701b">OnItemsChanged</a>
</td>
<td align="left" width="63%">

            Notifies the indexer to index changed items.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/97143616-05ed-4693-9a83-25ced1d6de07">StartedMonitoringScope</a>
</td>
<td align="left" width="63%">
Called by a notifications provider to notify the indexer to monitor changes to items within a specified hierarchical scope.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/18c01b84-4b31-4bf0-a48f-ede68aad604d">StoppedMonitoringScope</a>
</td>
<td align="left" width="63%">

            Called by a notifications provider to notify the indexer to stop monitoring changes to items within a specified hierarchical scope.
        

</td>
</tr>
</table> 


## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/817550e2-a256-48d5-9fa6-1ea04f8b8589">Notifying the Index of Changes</a>



<a href="https://msdn.microsoft.com/cfba12eb-4123-4b57-8311-d4fc8f9f514e">The Indexing Process</a>
 

 

