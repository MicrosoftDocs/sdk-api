---
UID: NF:searchapi.IRowsetPrioritization.SetScopePriority
title: IRowsetPrioritization::SetScopePriority (searchapi.h)
author: windows-sdk-content
description: Sets the current indexer prioritization level for the scope specified by this query.
old-location: search\_search_IRowsetPrioritization_SetScopePriority.htm
tech.root: search
ms.assetid: VS|SEARCH|~\search\wds3x\reference\ifaces\querying\irowsetprioritization\setscopepriority.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IRowsetPrioritization interface [search],SetScopePriority method, IRowsetPrioritization.SetScopePriority, IRowsetPrioritization::SetScopePriority, SetScopePriority, SetScopePriority method [search], SetScopePriority method [search],IRowsetPrioritization interface, _search_IRowsetPrioritization_SetScopePriority, search._search_IRowsetPrioritization_SetScopePriority, searchapi/IRowsetPrioritization::SetScopePriority
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
 - IRowsetPrioritization.SetScopePriority
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IRowsetPrioritization::SetScopePriority


## -description


Sets the current indexer prioritization level for the scope specified by this query.
        


## -parameters




### -param priority [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Dd797839(v=VS.85).aspx">PRIORITY_LEVEL</a></b>

Specifies the new indexer prioritization level to be set as the <a href="https://msdn.microsoft.com/en-us/library/Dd797839(v=VS.85).aspx">PRIORITY_LEVEL</a> enumeration.
        


### -param scopeStatisticsEventFrequency [in]

Type: <b>DWORD</b>

Specifies the occurrence interval of the scope statistics event when there are outstanding documents to be indexed within the query scopes.
        


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The SearchEvents code sample, available on <a href="http://go.microsoft.com/fwlink/p/?linkid=155654">Code Gallery</a> and the <a href="http://go.microsoft.com/fwlink/p/?linkid=129787">Windows 7 SDK</a>, demonstrates how to prioritize indexing events.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/Dd318749(v=VS.85).aspx">IRowsetEvents</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd318747(v=VS.85).aspx">IRowsetPrioritization</a>



<a href="https://msdn.microsoft.com/6cdfb7d3-f849-432c-960f-912e5024c583">Indexing Prioritization and Rowset Events in Windows 7</a>



<a href="https://msdn.microsoft.com/en-us/library/Cc142933(v=VS.85).aspx">PRIORITIZE_FLAGS</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd797839(v=VS.85).aspx">PRIORITY_LEVEL</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd368861(v=VS.85).aspx">ROWSETEVENT_ITEMSTATE</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd368862(v=VS.85).aspx">ROWSETEVENT_TYPE</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/Cc465173(v=VS.85).aspx">Rowset Properties</a>
 

 

