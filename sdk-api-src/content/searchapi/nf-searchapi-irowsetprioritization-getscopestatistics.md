---
UID: NF:searchapi.IRowsetPrioritization.GetScopeStatistics
title: IRowsetPrioritization::GetScopeStatistics
author: windows-sdk-content
description: Gets information describing the scope specified by this query.
old-location: search\_search_IRowsetPrioritization_GetScopeStatistics.htm
old-project: search
ms.assetid: VS|SEARCH|~\search\wds3x\reference\ifaces\querying\irowsetprioritization\getscopestatistics.htm
ms.author: windowssdkdev
ms.date: 06/08/2018
ms.keywords: GetScopeStatistics, GetScopeStatistics method [search], GetScopeStatistics method [search],IRowsetPrioritization interface, IRowsetPrioritization interface [search],GetScopeStatistics method, IRowsetPrioritization.GetScopeStatistics, IRowsetPrioritization::GetScopeStatistics, _search_IRowsetPrioritization_GetScopeStatistics, search._search_IRowsetPrioritization_GetScopeStatistics, searchapi/IRowsetPrioritization::GetScopeStatistics
ms.prod: windows
ms.technology: windows-sdk
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
 - IRowsetPrioritization.GetScopeStatistics
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
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



<a href="https://msdn.microsoft.com/library/Dd318749(v=VS.85).aspx">IRowsetEvents</a>



<a href="https://msdn.microsoft.com/library/Dd318747(v=VS.85).aspx">IRowsetPrioritization</a>



<a href="https://msdn.microsoft.com/6cdfb7d3-f849-432c-960f-912e5024c583">Indexing Prioritization and Rowset Events in Windows 7</a>



<a href="https://msdn.microsoft.com/library/Cc142933(v=VS.85).aspx">PRIORITIZE_FLAGS</a>



<a href="https://msdn.microsoft.com/library/Dd797839(v=VS.85).aspx">PRIORITY_LEVEL</a>



<a href="https://msdn.microsoft.com/library/Dd368861(v=VS.85).aspx">ROWSETEVENT_ITEMSTATE</a>



<a href="https://msdn.microsoft.com/library/Dd368862(v=VS.85).aspx">ROWSETEVENT_TYPE</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/library/Cc465173(v=VS.85).aspx">Rowset Properties</a>
 

 

