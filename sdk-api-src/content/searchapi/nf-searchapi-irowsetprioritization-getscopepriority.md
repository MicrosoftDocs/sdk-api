---
UID: NF:searchapi.IRowsetPrioritization.GetScopePriority
title: IRowsetPrioritization::GetScopePriority (searchapi.h)
description: Retrieves the current indexer prioritization level for the scope specified by this query.helpviewer_keywords: ["GetScopePriority","GetScopePriority method [search]","GetScopePriority method [search]","IRowsetPrioritization interface","IRowsetPrioritization interface [search]","GetScopePriority method","IRowsetPrioritization.GetScopePriority","IRowsetPrioritization::GetScopePriority","_search_IRowsetPrioritization_GetScopePriority","search._search_IRowsetPrioritization_GetScopePriority","searchapi/IRowsetPrioritization::GetScopePriority"]
old-location: search\_search_IRowsetPrioritization_GetScopePriority.htm
tech.root: search
ms.assetid: VS|SEARCH|~\search\wds3x\reference\ifaces\querying\irowsetprioritization\getscopepriority.htm
ms.date: 12/05/2018
ms.keywords: GetScopePriority, GetScopePriority method [search], GetScopePriority method [search],IRowsetPrioritization interface, IRowsetPrioritization interface [search],GetScopePriority method, IRowsetPrioritization.GetScopePriority, IRowsetPrioritization::GetScopePriority, _search_IRowsetPrioritization_GetScopePriority, search._search_IRowsetPrioritization_GetScopePriority, searchapi/IRowsetPrioritization::GetScopePriority
f1_keywords:
- searchapi/IRowsetPrioritization.GetScopePriority
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
- IRowsetPrioritization.GetScopePriority
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IRowsetPrioritization::GetScopePriority


## -description


Retrieves the current indexer prioritization level for the scope specified by this query.

        


## -parameters




### -param priority [out]

Type: <b><a href="https://docs.microsoft.com/windows/win32/api/searchapi/ne-searchapi-priority_level">PRIORITY_LEVEL</a>*</b>

The current indexer prioritization level as the <a href="https://docs.microsoft.com/windows/win32/api/searchapi/ne-searchapi-priority_level">PRIORITY_LEVEL</a> enumeration.
        


### -param scopeStatisticsEventFrequency [out]

Type: <b>DWORD*</b>

The occurrence interval of the scope statistics event when there are outstanding documents to be indexed within the query scopes.
        


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The SearchEvents code sample, available on <a href="https://code.msdn.microsoft.com/windowssearch">Code Gallery</a> and the <a href="https://msdn.microsoft.com/windowsvista/bb980924.aspx">Windows 7 SDK</a>, demonstrates how to prioritize indexing events.




## -see-also




<b>Conceptual</b>



<a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nn-searchapi-irowsetevents">IRowsetEvents</a>



<a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nn-searchapi-irowsetprioritization">IRowsetPrioritization</a>



<a href="https://docs.microsoft.com/windows/desktop/search/indexing-prioritization-and-rowset-events">Indexing Prioritization and Rowset Events in Windows 7</a>



<a href="https://docs.microsoft.com/windows/win32/api/searchapi/ne-searchapi-tagprioritize_flags">PRIORITIZE_FLAGS</a>



<a href="https://docs.microsoft.com/windows/win32/api/searchapi/ne-searchapi-priority_level">PRIORITY_LEVEL</a>



<a href="https://docs.microsoft.com/windows/win32/api/searchapi/ne-searchapi-rowsetevent_itemstate">ROWSETEVENT_ITEMSTATE</a>



<a href="https://docs.microsoft.com/windows/win32/api/searchapi/ne-searchapi-rowsetevent_type">ROWSETEVENT_TYPE</a>



<b>Reference</b>



<a href="https://docs.microsoft.com/windows/desktop/search/-search-sql-rowset-properties">Rowset Properties</a>
 

 

