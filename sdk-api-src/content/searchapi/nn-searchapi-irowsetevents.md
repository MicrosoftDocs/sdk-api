---
UID: NN:searchapi.IRowsetEvents
title: IRowsetEvents
author: windows-sdk-content
description: Exposes methods for receiving event notifications.
old-location: search\_search_IRowsetEvents.htm
tech.root: search
ms.assetid: VS|SEARCH|~\search\wds3x\reference\ifaces\querying\irowsetevents\irowsetevents.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IRowsetEvents, IRowsetEvents interface [search], IRowsetEvents interface [search],described, _search_IRowsetEvents, search._search_IRowsetEvents, searchapi/IRowsetEvents
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: searchapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Searchquery.idl
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
 - IRowsetEvents
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IRowsetEvents interface


## -description


Exposes methods for receiving event notifications. When clients implement this interface, the indexer can notify the clients of changes to items in their rowsets: including the addition of new items, the deletion of items, and the modifcation to item data.
            


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRowsetEvents</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IRowsetEvents</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IRowsetEvents</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd318750(v=VS.85).aspx">OnChangedItem</a>
</td>
<td align="left" width="63%">
Called by the indexer to notify clients that an item has been modified. This item may have matched some (or all) of the criteria for the client rowset.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd318751(v=VS.85).aspx">OnDeletedItem</a>
</td>
<td align="left" width="63%">
Called by the indexer to notify clients that an item has been deleted. This item may have matched some (or all) of the search criteria for the client rowset.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd318752(v=VS.85).aspx">OnNewItem</a>
</td>
<td align="left" width="63%">
Called by the indexer to notify clients of a new item that may match some (or all) of the criteria for the client rowset.
            
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd318753(v=VS.85).aspx">OnRowsetEvent</a>
</td>
<td align="left" width="63%">
Called by the indexer to notify clients of an event related to the client rowset.
            

</td>
</tr>
</table> 


## -remarks



<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
Implement <b>IRowsetEvents</b> if your provider needs to receive notifications of rowset events. <b>IRowsetEvents</b> exposes methods for receiving event notifications, and must be implemented to receive the following notifications on events: <a href="http://msdn.microsoft.com/en-us/library/dd318750(VS.85).aspx">OnChangedItem</a>, <a href="http://msdn.microsoft.com/en-us/library/dd318751(VS.85).aspx">OnDeletedItem</a>, <a href="http://msdn.microsoft.com/en-us/library/dd318752(VS.85).aspx">OnNewItem</a> and <a href="http://msdn.microsoft.com/en-us/library/dd318753(VS.85).aspx">OnRowsetEvent</a>. The <a href="https://msdn.microsoft.com/en-us/library/Dd368861(v=VS.85).aspx">ROWSETEVENT_ITEMSTATE</a> and <a href="https://msdn.microsoft.com/en-us/library/Dd368862(v=VS.85).aspx">ROWSETEVENT_TYPE</a> enumeratiors capture the item state and rowset event, respectively. 

Indexer eventing is a new feature for Windows 7 that allows providers to receive notifications on their rowsets. Providers can use eventing to maintain their rowsets in such a way that they behave akin to actual file system locations.

The <b>IRowsetEvents</b> interface is registered by connection point with an open indexer rowset.

<b>DBPROP_ENABLEROWSETEVENTS</b> must be set to <b>TRUE</b> with the OLE DB <a href="https://msdn.microsoft.com/library/ms711497(v=VS.85).aspx">ICommandProperties::SetProperties</a> method prior to executing the query in order to use rowset eventing.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/Dd318747(v=VS.85).aspx">IRowsetPrioritization</a>



<a href="https://msdn.microsoft.com/6cdfb7d3-f849-432c-960f-912e5024c583">Indexing Prioritization and Rowset Events in Windows 7</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb288457(v=VS.85).aspx">Notifications Process (Windows Search)</a>



<a href="https://msdn.microsoft.com/en-us/library/Cc142933(v=VS.85).aspx">PRIORITIZE_FLAGS</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd797839(v=VS.85).aspx">PRIORITY_LEVEL</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd368861(v=VS.85).aspx">ROWSETEVENT_ITEMSTATE</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd368862(v=VS.85).aspx">ROWSETEVENT_TYPE</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/Cc465173(v=VS.85).aspx">Rowset Properties</a>
 

 

