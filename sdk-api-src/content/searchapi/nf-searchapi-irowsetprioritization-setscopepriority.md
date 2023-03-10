---
UID: NF:searchapi.IRowsetPrioritization.SetScopePriority
title: IRowsetPrioritization::SetScopePriority (searchapi.h)
description: Sets the current indexer prioritization level for the scope specified by this query.
helpviewer_keywords: ["IRowsetPrioritization interface [search]","SetScopePriority method","IRowsetPrioritization.SetScopePriority","IRowsetPrioritization::SetScopePriority","SetScopePriority","SetScopePriority method [search]","SetScopePriority method [search]","IRowsetPrioritization interface","_search_IRowsetPrioritization_SetScopePriority","search._search_IRowsetPrioritization_SetScopePriority","searchapi/IRowsetPrioritization::SetScopePriority"]
old-location: search\_search_IRowsetPrioritization_SetScopePriority.htm
tech.root: search
ms.assetid: VS|SEARCH|~\search\wds3x\reference\ifaces\querying\irowsetprioritization\setscopepriority.htm
ms.date: 12/05/2018
ms.keywords: IRowsetPrioritization interface [search],SetScopePriority method, IRowsetPrioritization.SetScopePriority, IRowsetPrioritization::SetScopePriority, SetScopePriority, SetScopePriority method [search], SetScopePriority method [search],IRowsetPrioritization interface, _search_IRowsetPrioritization_SetScopePriority, search._search_IRowsetPrioritization_SetScopePriority, searchapi/IRowsetPrioritization::SetScopePriority
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
 - IRowsetPrioritization::SetScopePriority
 - searchapi/IRowsetPrioritization::SetScopePriority
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
 - IRowsetPrioritization.SetScopePriority
---

# IRowsetPrioritization::SetScopePriority


## -description

Sets the current indexer prioritization level for the scope specified by this query.

## -parameters

### -param priority [in]

Type: <b><a href="/windows/win32/api/searchapi/ne-searchapi-priority_level">PRIORITY_LEVEL</a></b>

Specifies the new indexer prioritization level to be set as the <a href="/windows/win32/api/searchapi/ne-searchapi-priority_level">PRIORITY_LEVEL</a> enumeration.

### -param scopeStatisticsEventFrequency [in]

Type: <b>DWORD</b>

Specifies the occurrence interval of the scope statistics event when there are outstanding documents to be indexed within the query scopes.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Check out the <a href="/windows/win32/search/-search-sample-searchevents">SearchEvents code sample</a>.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/searchapi/nn-searchapi-irowsetevents">IRowsetEvents</a>



<a href="/windows/desktop/api/searchapi/nn-searchapi-irowsetprioritization">IRowsetPrioritization</a>



<a href="/windows/desktop/search/indexing-prioritization-and-rowset-events">Indexing Prioritization and Rowset Events in Windows 7</a>



<a href="/windows/win32/api/searchapi/ne-searchapi-tagprioritize_flags">PRIORITIZE_FLAGS</a>



<a href="/windows/win32/api/searchapi/ne-searchapi-priority_level">PRIORITY_LEVEL</a>



<a href="/windows/win32/api/searchapi/ne-searchapi-rowsetevent_itemstate">ROWSETEVENT_ITEMSTATE</a>



<a href="/windows/win32/api/searchapi/ne-searchapi-rowsetevent_type">ROWSETEVENT_TYPE</a>



<b>Reference</b>



<a href="/windows/desktop/search/-search-sql-rowset-properties">Rowset Properties</a>