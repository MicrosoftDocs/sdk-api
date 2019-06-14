---
UID: NN:searchapi.IRowsetEvents
title: IRowsetEvents (searchapi.h)
author: windows-sdk-content
description: Exposes methods for receiving event notifications.
old-location: search\_search_IRowsetEvents.htm
tech.root: search
ms.assetid: VS|SEARCH|~\search\wds3x\reference\ifaces\querying\irowsetevents\irowsetevents.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IRowsetEvents, IRowsetEvents interface [search], IRowsetEvents interface [search],described, _search_IRowsetEvents, search._search_IRowsetEvents, searchapi/IRowsetEvents
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
ms.custom: 19H1
---

# IRowsetEvents interface


## -description


Exposes methods for receiving event notifications. When clients implement this interface, the indexer can notify the clients of changes to items in their rowsets: including the addition of new items, the deletion of items, and the modifcation to item data.
            


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRowsetEvents</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IRowsetEvents</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nf-searchapi-irowsetevents-onchangeditem">OnChangedItem</a>
</td>
<td align="left" width="63%">
Called by the indexer to notify clients that an item has been modified. This item may have matched some (or all) of the criteria for the client rowset.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nf-searchapi-irowsetevents-ondeleteditem">OnDeletedItem</a>
</td>
<td align="left" width="63%">
Called by the indexer to notify clients that an item has been deleted. This item may have matched some (or all) of the search criteria for the client rowset.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nf-searchapi-irowsetevents-onnewitem">OnNewItem</a>
</td>
<td align="left" width="63%">
Called by the indexer to notify clients of a new item that may match some (or all) of the criteria for the client rowset.
            
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nf-searchapi-irowsetevents-onrowsetevent">OnRowsetEvent</a>
</td>
<td align="left" width="63%">
Called by the indexer to notify clients of an event related to the client rowset.
            

</td>
</tr>
</table> 


## -remarks



<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
Implement <b>IRowsetEvents</b> if your provider needs to receive notifications of rowset events. <b>IRowsetEvents</b> exposes methods for receiving event notifications, and must be implemented to receive the following notifications on events: <a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nf-searchapi-irowsetevents-onchangeditem">OnChangedItem</a>, <a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nf-searchapi-irowsetevents-ondeleteditem">OnDeletedItem</a>, <a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nf-searchapi-irowsetevents-onnewitem">OnNewItem</a> and <a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nf-searchapi-irowsetevents-onrowsetevent">OnRowsetEvent</a>. The <a href="https://docs.microsoft.com/windows/desktop/api/searchapi/ne-searchapi-__midl___midl_itf_searchapi_0000_0023_0001">ROWSETEVENT_ITEMSTATE</a> and <a href="https://docs.microsoft.com/windows/desktop/api/searchapi/ne-searchapi-__midl___midl_itf_searchapi_0000_0023_0002">ROWSETEVENT_TYPE</a> enumeratiors capture the item state and rowset event, respectively. 

Indexer eventing is a new feature for Windows 7 that allows providers to receive notifications on their rowsets. Providers can use eventing to maintain their rowsets in such a way that they behave akin to actual file system locations.

The <b>IRowsetEvents</b> interface is registered by connection point with an open indexer rowset.

<b>DBPROP_ENABLEROWSETEVENTS</b> must be set to <b>TRUE</b> with the OLE DB <a href="https://docs.microsoft.com/previous-versions/windows/desktop/ms711497(v=vs.85)">ICommandProperties::SetProperties</a> method prior to executing the query in order to use rowset eventing.




## -see-also




<b>Conceptual</b>



<a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nn-searchapi-irowsetprioritization">IRowsetPrioritization</a>



<a href="https://docs.microsoft.com/windows/desktop/search/indexing-prioritization-and-rowset-events">Indexing Prioritization and Rowset Events in Windows 7</a>



<a href="https://docs.microsoft.com/windows/desktop/search/-search-3x-wds-support">Notifications Process (Windows Search)</a>



<a href="https://docs.microsoft.com/windows/desktop/api/searchapi/ne-searchapi-tagprioritize_flags">PRIORITIZE_FLAGS</a>



<a href="https://docs.microsoft.com/windows/desktop/api/searchapi/ne-searchapi-__midl___midl_itf_searchapi_0000_0022_0001">PRIORITY_LEVEL</a>



<a href="https://docs.microsoft.com/windows/desktop/api/searchapi/ne-searchapi-__midl___midl_itf_searchapi_0000_0023_0001">ROWSETEVENT_ITEMSTATE</a>



<a href="https://docs.microsoft.com/windows/desktop/api/searchapi/ne-searchapi-__midl___midl_itf_searchapi_0000_0023_0002">ROWSETEVENT_TYPE</a>



<b>Reference</b>



<a href="https://docs.microsoft.com/windows/desktop/search/-search-sql-rowset-properties">Rowset Properties</a>
 

 

