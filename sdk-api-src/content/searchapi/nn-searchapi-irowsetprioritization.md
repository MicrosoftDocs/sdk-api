---
UID: NN:searchapi.IRowsetPrioritization
title: IRowsetPrioritization (searchapi.h)
author: windows-sdk-content
description: Sets or retrieves the current indexer prioritization level for the scope specified by this query.
old-location: search\_search_IRowsetPrioritization.htm
tech.root: search
ms.assetid: VS|SEARCH|~\search\wds3x\reference\ifaces\querying\irowsetprioritization\irowsetprioritization.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IRowsetPrioritization, IRowsetPrioritization interface [search], IRowsetPrioritization interface [search],described, _search_IRowsetPrioritization, search._search_IRowsetPrioritization, searchapi/IRowsetPrioritization
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
 - IRowsetPrioritization
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IRowsetPrioritization interface


## -description


Sets or retrieves the current indexer prioritization level for the scope specified by this query.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRowsetPrioritization</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IRowsetPrioritization</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/en-us/library/Dd318299(v=VS.85).aspx">GetScopePriority</a>
</td>
<td align="left" width="63%">
Retrieves the current indexer prioritization level for the scope specified by this query.

        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd318746(v=VS.85).aspx">GetScopeStatistics</a>
</td>
<td align="left" width="63%">
Gets information describing the scope specified by this query.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd318748(v=VS.85).aspx">SetScopePriority</a>
</td>
<td align="left" width="63%">
Sets the current indexer prioritization level for the scope specified by this query.
        

</td>
</tr>
</table> 


## -remarks



This interface is acquired with <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">IUnknown::QueryInterface Method</a> on an indexer rowset. <b>DBPROP_ENABLEROWSETEVENTS</b> must be set to <b>TRUE</b> with the OLE DB <a href="https://msdn.microsoft.com/library/ms711497(v=VS.85).aspx">ICommandProperties::SetProperties</a> method prior to executing the query in order to use rowset prioritization.


<a href="https://msdn.microsoft.com/en-us/library/Dd318748(v=VS.85).aspx">IRowsetPrioritization::SetScopePriority</a> sets the prioritization for the scopes belonging to the query, and the interval the scope statistics event is raised when there are outstanding documents to be indexed within the query scopes. This event is raised if the priority level is set to default.


<a href="https://msdn.microsoft.com/en-us/library/Dd318746(v=VS.85).aspx">IRowsetPrioritization::GetScopeStatistics</a> can be used to get the number of indexed items in the scope, the number of outstanding documents to be added in the scope, and the number of documents that need to be re-indexed within this scope.

The SearchEvents code sample, available on <a href="http://go.microsoft.com/fwlink/p/?linkid=155654">Code Gallery</a> and the <a href="http://go.microsoft.com/fwlink/p/?linkid=129787">Windows 7 SDK</a>, demonstrates how to prioritize indexing events.
        




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/Dd318749(v=VS.85).aspx">IRowsetEvents</a>



<a href="https://msdn.microsoft.com/6cdfb7d3-f849-432c-960f-912e5024c583">Indexing Prioritization and Rowset Events in Windows 7</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb288457(v=VS.85).aspx">Notifications Process (Windows Search)</a>



<a href="https://msdn.microsoft.com/en-us/library/Cc142933(v=VS.85).aspx">PRIORITIZE_FLAGS</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd797839(v=VS.85).aspx">PRIORITY_LEVEL</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd368861(v=VS.85).aspx">ROWSETEVENT_ITEMSTATE</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd368862(v=VS.85).aspx">ROWSETEVENT_TYPE</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/Cc465173(v=VS.85).aspx">Rowset Properties</a>
 

 

