---
UID: NN:searchapi.IRowsetPrioritization
title: IRowsetPrioritization
author: windows-sdk-content
description: Sets or retrieves the current indexer prioritization level for the scope specified by this query.
old-location: search\_search_IRowsetPrioritization.htm
old-project: search
ms.assetid: VS|SEARCH|~\search\wds3x\reference\ifaces\querying\irowsetprioritization\irowsetprioritization.htm
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: IRowsetPrioritization, IRowsetPrioritization interface [search], IRowsetPrioritization interface [search],described, _search_IRowsetPrioritization, search._search_IRowsetPrioritization, searchapi/IRowsetPrioritization
ms.prod: windows
ms.technology: windows-sdk
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
 - IRowsetPrioritization
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
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
<a href="https://msdn.microsoft.com/89d1f23d-5f22-40c5-bf0b-3a529897cc96">GetScopePriority</a>
</td>
<td align="left" width="63%">
Retrieves the current indexer prioritization level for the scope specified by this query.

        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/82d64fe6-6264-4262-a778-bf30a62dcecb">GetScopeStatistics</a>
</td>
<td align="left" width="63%">
Gets information describing the scope specified by this query.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a7a11343-c8ba-4cbd-bc7a-a0de65b99003">SetScopePriority</a>
</td>
<td align="left" width="63%">
Sets the current indexer prioritization level for the scope specified by this query.
        

</td>
</tr>
</table> 


## -remarks



This interface is acquired with <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">IUnknown::QueryInterface Method</a> on an indexer rowset. <b>DBPROP_ENABLEROWSETEVENTS</b> must be set to <b>TRUE</b> with the OLE DB <a href="1e2f5e85-459e-4588-a6fa-4209d5a667c4">ICommandProperties::SetProperties</a> method prior to executing the query in order to use rowset prioritization.


<a href="https://msdn.microsoft.com/a7a11343-c8ba-4cbd-bc7a-a0de65b99003">IRowsetPrioritization::SetScopePriority</a> sets the prioritization for the scopes belonging to the query, and the interval the scope statistics event is raised when there are outstanding documents to be indexed within the query scopes. This event is raised if the priority level is set to default.


<a href="https://msdn.microsoft.com/82d64fe6-6264-4262-a778-bf30a62dcecb">IRowsetPrioritization::GetScopeStatistics</a> can be used to get the number of indexed items in the scope, the number of outstanding documents to be added in the scope, and the number of documents that need to be re-indexed within this scope.

The SearchEvents code sample, available on <a href="http://go.microsoft.com/fwlink/p/?linkid=155654">Code Gallery</a> and the <a href="http://go.microsoft.com/fwlink/p/?linkid=129787">Windows 7 SDK</a>, demonstrates how to prioritize indexing events.
        




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/df16492c-e8f9-4d01-a8ad-cd76ea6bbc73">IRowsetEvents</a>



<a href="https://msdn.microsoft.com/6cdfb7d3-f849-432c-960f-912e5024c583">Indexing Prioritization and Rowset Events in Windows 7</a>



<a href="https://msdn.microsoft.com/378e346b-2067-484f-85e9-76673a35550b">Notifications Process (Windows Search)</a>



<a href="https://msdn.microsoft.com/554d405e-c117-4597-9612-20cd6088ebef">PRIORITIZE_FLAGS</a>



<a href="https://msdn.microsoft.com/d172ae7f-a495-4ea4-9d7d-ca8065f8d3cb">PRIORITY_LEVEL</a>



<a href="https://msdn.microsoft.com/2df331c6-9048-4720-b582-0025461134c1">ROWSETEVENT_ITEMSTATE</a>



<a href="https://msdn.microsoft.com/c9fb74f6-8aed-4450-9bc4-d9f5c3e835a4">ROWSETEVENT_TYPE</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/71aa0ad6-ef34-47ee-945f-04bda20bf8a4">Rowset Properties</a>
 

 

