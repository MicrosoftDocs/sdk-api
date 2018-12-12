---
UID: NF:searchapi.IRowsetPrioritization.GetScopeStatistics
title: IRowsetPrioritization::GetScopeStatistics
author: windows-sdk-content
description: Gets information describing the scope specified by this query.
old-location: search\_search_IRowsetPrioritization_GetScopeStatistics.htm
tech.root: search
ms.assetid: VS|SEARCH|~\search\wds3x\reference\ifaces\querying\irowsetprioritization\getscopestatistics.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetScopeStatistics, GetScopeStatistics method [search], GetScopeStatistics method [search],IRowsetPrioritization interface, IRowsetPrioritization interface [search],GetScopeStatistics method, IRowsetPrioritization.GetScopeStatistics, IRowsetPrioritization::GetScopeStatistics, _search_IRowsetPrioritization_GetScopeStatistics, search._search_IRowsetPrioritization_GetScopeStatistics, searchapi/IRowsetPrioritization::GetScopeStatistics
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IRowsetPrioritization.GetScopeStatistics
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Returns S_OK if successful, <b>HRESULT_FROM_WIN32(ERROR_PATH_NOT_FOUND)</b> if there are no indexed documents in the scope, or an error value otherwise.

The <b>GetScopeStatistics</b> event can be used to get the number of indexed items in the scope, the number of outstanding docs to be added in the scope, and the number of docs that need to be re-indexed within this scope.

The SearchEvents code sample, available on <a href="http://go.microsoft.com/fwlink/p/?linkid=155654">Code Gallery</a> and the <a href="http://go.microsoft.com/fwlink/p/?linkid=129787">Windows 7 SDK</a>, demonstrates how to prioritize indexing events.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/df16492c-e8f9-4d01-a8ad-cd76ea6bbc73">IRowsetEvents</a>



<a href="https://msdn.microsoft.com/82dce1fa-9bc5-4744-966e-1e7aa6fc3e05">IRowsetPrioritization</a>



<a href="https://msdn.microsoft.com/6cdfb7d3-f849-432c-960f-912e5024c583">Indexing Prioritization and Rowset Events in Windows 7</a>



<a href="https://msdn.microsoft.com/554d405e-c117-4597-9612-20cd6088ebef">PRIORITIZE_FLAGS</a>



<a href="https://msdn.microsoft.com/d172ae7f-a495-4ea4-9d7d-ca8065f8d3cb">PRIORITY_LEVEL</a>



<a href="https://msdn.microsoft.com/2df331c6-9048-4720-b582-0025461134c1">ROWSETEVENT_ITEMSTATE</a>



<a href="https://msdn.microsoft.com/c9fb74f6-8aed-4450-9bc4-d9f5c3e835a4">ROWSETEVENT_TYPE</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/71aa0ad6-ef34-47ee-945f-04bda20bf8a4">Rowset Properties</a>
 

 

