---
UID: NN:searchapi.IRowsetEvents
title: IRowsetEvents (searchapi.h)
description: Exposes methods for receiving event notifications.
helpviewer_keywords: ["IRowsetEvents","IRowsetEvents interface [search]","IRowsetEvents interface [search]","described","_search_IRowsetEvents","search._search_IRowsetEvents","searchapi/IRowsetEvents"]
old-location: search\_search_IRowsetEvents.htm
tech.root: search
ms.assetid: VS|SEARCH|~\search\wds3x\reference\ifaces\querying\irowsetevents\irowsetevents.htm
ms.date: 12/05/2018
ms.keywords: IRowsetEvents, IRowsetEvents interface [search], IRowsetEvents interface [search],described, _search_IRowsetEvents, search._search_IRowsetEvents, searchapi/IRowsetEvents
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IRowsetEvents
 - searchapi/IRowsetEvents
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
 - IRowsetEvents
---

# IRowsetEvents interface


## -description

Exposes methods for receiving event notifications. When clients implement this interface, the indexer can notify the clients of changes to items in their rowsets: including the addition of new items, the deletion of items, and the modification to item data.

## -inheritance

The <b>IRowsetEvents</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IRowsetEvents</b> also has these types of members:

## -remarks

<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
Implement <b>IRowsetEvents</b> if your provider needs to receive notifications of rowset events. <b>IRowsetEvents</b> exposes methods for receiving event notifications, and must be implemented to receive the following notifications on events: <a href="/windows/win32/api/searchapi/ne-searchapi-rowsetevent_itemstate">OnChangedItem</a>, <a href="/windows/desktop/api/searchapi/nf-searchapi-irowsetevents-ondeleteditem">OnDeletedItem</a>, <a href="/windows/desktop/api/searchapi/nf-searchapi-irowsetevents-onnewitem">OnNewItem</a> and <a href="/windows/desktop/api/searchapi/nf-searchapi-irowsetevents-onrowsetevent">OnRowsetEvent</a>. The <a href="/windows/win32/api/searchapi/ne-searchapi-rowsetevent_itemstate">ROWSETEVENT_ITEMSTATE</a> and <a href="/windows/win32/api/searchapi/ne-searchapi-rowsetevent_type">ROWSETEVENT_TYPE</a> enumerators capture the item state and rowset event, respectively. 

Indexer eventing is a new feature for Windows 7 that allows providers to receive notifications on their rowsets. Providers can use eventing to maintain their rowsets in such a way that they behave akin to actual file system locations.

The <b>IRowsetEvents</b> interface is registered by connection point with an open indexer rowset.

<b>DBPROP_ENABLEROWSETEVENTS</b> must be set to <b>TRUE</b> with the OLE DB <a href="/previous-versions/windows/desktop/ms711497(v=vs.85)">ICommandProperties::SetProperties</a> method prior to executing the query in order to use rowset eventing.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/searchapi/nn-searchapi-irowsetprioritization">IRowsetPrioritization</a>



<a href="/windows/desktop/search/indexing-prioritization-and-rowset-events">Indexing Prioritization and Rowset Events in Windows 7</a>



<a href="/windows/desktop/search/-search-3x-wds-support">Notifications Process (Windows Search)</a>



<a href="/windows/win32/api/searchapi/ne-searchapi-tagprioritize_flags">PRIORITIZE_FLAGS</a>



<a href="/windows/win32/api/searchapi/ne-searchapi-priority_level">PRIORITY_LEVEL</a>



<a href="/windows/win32/api/searchapi/ne-searchapi-rowsetevent_itemstate">ROWSETEVENT_ITEMSTATE</a>



<a href="/windows/win32/api/searchapi/ne-searchapi-rowsetevent_type">ROWSETEVENT_TYPE</a>



<b>Reference</b>



<a href="/windows/desktop/search/-search-sql-rowset-properties">Rowset Properties</a>
