---
UID: NN:searchapi.IRowsetPrioritization
title: IRowsetPrioritization (searchapi.h)
description: Sets or retrieves the current indexer prioritization level for the scope specified by this query.
old-location: search\_search_IRowsetPrioritization.htm
tech.root: search
ms.assetid: VS|SEARCH|~\search\wds3x\reference\ifaces\querying\irowsetprioritization\irowsetprioritization.htm
ms.date: 12/05/2018
ms.keywords: IRowsetPrioritization, IRowsetPrioritization interface [search], IRowsetPrioritization interface [search],described, _search_IRowsetPrioritization, search._search_IRowsetPrioritization, searchapi/IRowsetPrioritization
ms.topic: interface
f1_keywords:
- searchapi/IRowsetPrioritization
dev_langs:
- c++
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
- IRowsetPrioritization
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IRowsetPrioritization interface


## -description


Sets or retrieves the current indexer prioritization level for the scope specified by this query.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRowsetPrioritization</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IRowsetPrioritization</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IRowsetPrioritization</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nf-searchapi-irowsetprioritization-getscopepriority">GetScopePriority</a>
</td>
<td align="left" width="63%">
Retrieves the current indexer prioritization level for the scope specified by this query.

        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nf-searchapi-irowsetprioritization-getscopestatistics">GetScopeStatistics</a>
</td>
<td align="left" width="63%">
Gets information describing the scope specified by this query.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nf-searchapi-irowsetprioritization-setscopepriority">SetScopePriority</a>
</td>
<td align="left" width="63%">
Sets the current indexer prioritization level for the scope specified by this query.
        

</td>
</tr>
</table> 


## -remarks



This interface is acquired with <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q_)">IUnknown::QueryInterface Method</a> on an indexer rowset. <b>DBPROP_ENABLEROWSETEVENTS</b> must be set to <b>TRUE</b> with the OLE DB <a href="https://docs.microsoft.com/previous-versions/windows/desktop/ms711497(v=vs.85)">ICommandProperties::SetProperties</a> method prior to executing the query in order to use rowset prioritization.


<a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nf-searchapi-irowsetprioritization-setscopepriority">IRowsetPrioritization::SetScopePriority</a> sets the prioritization for the scopes belonging to the query, and the interval the scope statistics event is raised when there are outstanding documents to be indexed within the query scopes. This event is raised if the priority level is set to default.


<a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nf-searchapi-irowsetprioritization-getscopestatistics">IRowsetPrioritization::GetScopeStatistics</a> can be used to get the number of indexed items in the scope, the number of outstanding documents to be added in the scope, and the number of documents that need to be re-indexed within this scope.

The SearchEvents code sample, available on <a href="http://go.microsoft.com/fwlink/p/?linkid=155654">Code Gallery</a> and the <a href="http://go.microsoft.com/fwlink/p/?linkid=129787">Windows 7 SDK</a>, demonstrates how to prioritize indexing events.
        




## -see-also




<b>Conceptual</b>



<a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nn-searchapi-irowsetevents">IRowsetEvents</a>



<a href="https://docs.microsoft.com/windows/desktop/search/indexing-prioritization-and-rowset-events">Indexing Prioritization and Rowset Events in Windows 7</a>



<a href="https://docs.microsoft.com/windows/desktop/search/-search-3x-wds-support">Notifications Process (Windows Search)</a>



<a href="https://docs.microsoft.com/windows/win32/api/searchapi/ne-searchapi-tagprioritize_flags">PRIORITIZE_FLAGS</a>



<a href="https://docs.microsoft.com/windows/win32/api/searchapi/ne-searchapi-priority_level">PRIORITY_LEVEL</a>



<a href="https://docs.microsoft.com/windows/win32/api/searchapi/ne-searchapi-rowsetevent_itemstate">ROWSETEVENT_ITEMSTATE</a>



<a href="https://docs.microsoft.com/windows/win32/api/searchapi/ne-searchapi-rowsetevent_type">ROWSETEVENT_TYPE</a>



<b>Reference</b>



<a href="https://docs.microsoft.com/windows/desktop/search/-search-sql-rowset-properties">Rowset Properties</a>
 

 

