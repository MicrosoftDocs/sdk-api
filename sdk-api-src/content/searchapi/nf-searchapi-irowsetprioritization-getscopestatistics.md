---
UID: NF:searchapi.IRowsetPrioritization.GetScopeStatistics
title: IRowsetPrioritization::GetScopeStatistics (searchapi.h)
description: Gets information describing the scope specified by this query.
helpviewer_keywords: ["GetScopeStatistics","GetScopeStatistics method [search]","GetScopeStatistics method [search]","IRowsetPrioritization interface","IRowsetPrioritization interface [search]","GetScopeStatistics method","IRowsetPrioritization.GetScopeStatistics","IRowsetPrioritization::GetScopeStatistics","_search_IRowsetPrioritization_GetScopeStatistics","search._search_IRowsetPrioritization_GetScopeStatistics","searchapi/IRowsetPrioritization::GetScopeStatistics"]
old-location: search\_search_IRowsetPrioritization_GetScopeStatistics.htm
tech.root: search
ms.assetid: VS|SEARCH|~\search\wds3x\reference\ifaces\querying\irowsetprioritization\getscopestatistics.htm
ms.date: 12/05/2018
ms.keywords: GetScopeStatistics, GetScopeStatistics method [search], GetScopeStatistics method [search],IRowsetPrioritization interface, IRowsetPrioritization interface [search],GetScopeStatistics method, IRowsetPrioritization.GetScopeStatistics, IRowsetPrioritization::GetScopeStatistics, _search_IRowsetPrioritization_GetScopeStatistics, search._search_IRowsetPrioritization_GetScopeStatistics, searchapi/IRowsetPrioritization::GetScopeStatistics
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
 - IRowsetPrioritization::GetScopeStatistics
 - searchapi/IRowsetPrioritization::GetScopeStatistics
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
 - IRowsetPrioritization.GetScopeStatistics
---

# IRowsetPrioritization::GetScopeStatistics


## -description

Gets information describing the scope specified by this query.

## -parameters

### -param indexedDocumentCount [out]

Type: <b>DWORD*</b>

The total number of documents currently indexed in the scope.

### -param oustandingAddCount [out]

Type: <b>DWORD*</b>

The total number of documents yet to be indexed in the scope. These documents are not yet included in <i>indexedDocumentCount</i>.

### -param oustandingModifyCount [out]

Type: <b>DWORD*</b>

The total number of documents indexed in the scope that need to be re-indexed. These documents are included in <i>indexedDocumentCount</i>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Returns S_OK if successful, <b>HRESULT_FROM_WIN32(ERROR_PATH_NOT_FOUND)</b> if there are no indexed documents in the scope, or an error value otherwise.

The <b>GetScopeStatistics</b> event can be used to get the number of indexed items in the scope, the number of outstanding docs to be added in the scope, and the number of docs that need to be re-indexed within this scope.

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