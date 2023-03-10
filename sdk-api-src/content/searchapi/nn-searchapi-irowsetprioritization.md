---
UID: NN:searchapi.IRowsetPrioritization
title: IRowsetPrioritization (searchapi.h)
description: Sets or retrieves the current indexer prioritization level for the scope specified by this query.
helpviewer_keywords: ["IRowsetPrioritization","IRowsetPrioritization interface [search]","IRowsetPrioritization interface [search]","described","_search_IRowsetPrioritization","search._search_IRowsetPrioritization","searchapi/IRowsetPrioritization"]
old-location: search\_search_IRowsetPrioritization.htm
tech.root: search
ms.assetid: VS|SEARCH|~\search\wds3x\reference\ifaces\querying\irowsetprioritization\irowsetprioritization.htm
ms.date: 12/05/2018
ms.keywords: IRowsetPrioritization, IRowsetPrioritization interface [search], IRowsetPrioritization interface [search],described, _search_IRowsetPrioritization, search._search_IRowsetPrioritization, searchapi/IRowsetPrioritization
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
 - IRowsetPrioritization
 - searchapi/IRowsetPrioritization
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
 - IRowsetPrioritization
---

# IRowsetPrioritization interface


## -description

Sets or retrieves the current indexer prioritization level for the scope specified by this query.

## -inheritance

The <b>IRowsetPrioritization</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IRowsetPrioritization</b> also has these types of members:

## -remarks

This interface is acquired with <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">IUnknown::QueryInterface Method</a> on an indexer rowset. <b>DBPROP_ENABLEROWSETEVENTS</b> must be set to <b>TRUE</b> with the OLE DB <a href="/previous-versions/windows/desktop/ms711497(v=vs.85)">ICommandProperties::SetProperties</a> method prior to executing the query in order to use rowset prioritization.


<a href="/windows/desktop/api/searchapi/nf-searchapi-irowsetprioritization-setscopepriority">IRowsetPrioritization::SetScopePriority</a> sets the prioritization for the scopes belonging to the query, and the interval the scope statistics event is raised when there are outstanding documents to be indexed within the query scopes. This event is raised if the priority level is set to default.


<a href="/windows/desktop/api/searchapi/nf-searchapi-irowsetprioritization-getscopestatistics">IRowsetPrioritization::GetScopeStatistics</a> can be used to get the number of indexed items in the scope, the number of outstanding documents to be added in the scope, and the number of documents that need to be re-indexed within this scope.

For a sample that demonstrates how to prioritize indexing events, see the [SearchEvents](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/SearchEvents) sample.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/searchapi/nn-searchapi-irowsetevents">IRowsetEvents</a>



<a href="/windows/desktop/search/indexing-prioritization-and-rowset-events">Indexing Prioritization and Rowset Events in Windows 7</a>



<a href="/windows/desktop/search/-search-3x-wds-support">Notifications Process (Windows Search)</a>



<a href="/windows/win32/api/searchapi/ne-searchapi-tagprioritize_flags">PRIORITIZE_FLAGS</a>



<a href="/windows/win32/api/searchapi/ne-searchapi-priority_level">PRIORITY_LEVEL</a>



<a href="/windows/win32/api/searchapi/ne-searchapi-rowsetevent_itemstate">ROWSETEVENT_ITEMSTATE</a>



<a href="/windows/win32/api/searchapi/ne-searchapi-rowsetevent_type">ROWSETEVENT_TYPE</a>



<b>Reference</b>



<a href="/windows/desktop/search/-search-sql-rowset-properties">Rowset Properties</a>
