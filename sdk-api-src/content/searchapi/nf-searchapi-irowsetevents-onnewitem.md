---
UID: NF:searchapi.IRowsetEvents.OnNewItem
title: IRowsetEvents::OnNewItem method
author: windows-driver-content
description: Called by the indexer to notify clients of a new item that may match some (or all) of the criteria for the client rowset.
old-location: search\_search_IRowsetEvents_OnNewItem.htm
old-project: search
ms.assetid: VS|SEARCH|~\search\wds3x\reference\ifaces\querying\irowsetevents\onnewitem.htm
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: IRowsetEvents, IRowsetEvents interface [search], OnNewItem method, IRowsetEvents::OnNewItem, OnNewItem method [search], OnNewItem method [search], IRowsetEvents interface, OnNewItem,IRowsetEvents.OnNewItem, _search_IRowsetEvents_OnNewItem, search._search_IRowsetEvents_OnNewItem, searchapi/IRowsetEvents::OnNewItem
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
req.typenames: ROWSETEVENT_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Searchapi.h
api_name:
-	IRowsetEvents.OnNewItem
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IRowsetEvents::OnNewItem method


## -description


Called by the indexer to notify clients of a new item that may match some (or all) of the criteria for the client rowset.
            
        


## -parameters




### -param itemID [in]

Type: <b>REFPROPVARIANT</b>


            The new item that may match the original search criteria of the rowset.
        


### -param newItemState [in]

Type: <b><a href="https://msdn.microsoft.com/2df331c6-9048-4720-b582-0025461134c1">ROWSETEVENT_ITEMSTATE</a></b>


            Specifies whether the new item matches all or some of the criteria for your rowset, as a <a href="https://msdn.microsoft.com/2df331c6-9048-4720-b582-0025461134c1">ROWSETEVENT_ITEMSTATE</a> enumeration.
        


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The <a href="https://msdn.microsoft.com/2df331c6-9048-4720-b582-0025461134c1">ROWSETEVENT_ITEMSTATE</a> indicates the degree to which the new item may match the original search criteria of a rowset:
        

<ul>
<li><i>ROWSETEVENT_ITEMSTATE_INROWSET</i> indicates that the new item definitely matches all criteria for your rowset.</li>
<li><i>ROWSETEVENT_ITEMSTATE_UNKNOWN</i> indicates that the new item at least partially matches some criteria for your rowset. It may match fully.</li>
<li><i>ROWSETEVENT_ITEMSTATE_NOTINROWSET</i> is not applicable for new items.</li>
</ul>



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
 

 

