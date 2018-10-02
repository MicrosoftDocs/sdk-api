---
UID: NF:searchapi.IRowsetEvents.OnChangedItem
title: IRowsetEvents::OnChangedItem
author: windows-sdk-content
description: Called by the indexer to notify clients that an item has been modified. This item may have matched some (or all) of the criteria for the client rowset.
old-location: search\_search_IRowsetEvents_OnChangedItem.htm
tech.root: search
ms.assetid: VS|SEARCH|~\search\wds3x\reference\ifaces\querying\irowsetevents\onchangeditem.htm
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: IRowsetEvents interface [search],OnChangedItem method, IRowsetEvents.OnChangedItem, IRowsetEvents::OnChangedItem, OnChangedItem, OnChangedItem method [search], OnChangedItem method [search],IRowsetEvents interface, _search_IRowsetEvents_OnChangedItem, search._search_IRowsetEvents_OnChangedItem, searchapi/IRowsetEvents::OnChangedItem
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
 - IRowsetEvents.OnChangedItem
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IRowsetEvents::OnChangedItem


## -description


Called by the indexer to notify clients that an item has been modified. This item may have matched some (or all) of the criteria for the client rowset.
        


## -parameters




### -param itemID [in]

Type: <b>REFPROPVARIANT</b>

Specifies the item in the rowset that has changed.
        


### -param rowsetItemState [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Dd368861(v=VS.85).aspx">ROWSETEVENT_ITEMSTATE</a></b>

Specifies whether the changed item was originally in the rowset.
        


### -param changedItemState [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Dd368861(v=VS.85).aspx">ROWSETEVENT_ITEMSTATE</a></b>

Specifies whether the changed item is currently in the rowset, as a result of the change.
        


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The <a href="https://msdn.microsoft.com/en-us/library/Dd368861(v=VS.85).aspx">ROWSETEVENT_ITEMSTATE</a> for <i>rowsetItemState</i> indicates whether the item was contained in the original rowset: 

<ul>
<li><i>ROWSETEVENT_ITEMSTATE_INROWSET</i> indicates that the item is definitely contained within your rowset.</li>
<li><i>ROWSETEVENT_ITEMSTATE_UNKNOWN</i> indicates that the item may be contained within your rowset. The containment status is not known because your rowset is not fully evaluated.</li>
<li><i>ROWSETEVENT_ITEMSTATE_NOTINROWSET</i> indicates indicates that the item was not originally in your rowset</li>
</ul>
The <a href="https://msdn.microsoft.com/en-us/library/Dd368861(v=VS.85).aspx">ROWSETEVENT_ITEMSTATE</a> for <i>changedItemState</i> indicates whether the newly modified item now matches the degree to which the new item may match the original search criteria of a rowset: 

<ul>
<li><i>ROWSETEVENT_ITEMSTATE_INROWSET</i> indicates that the item definitely belongs in your rowset.</li>
<li><i>ROWSETEVENT_ITEMSTATE_UNKNOWN</i> indicates that the item may now belong in your rowset.</li>
<li><i>ROWSETEVENT_ITEMSTATE_NOTINROWSET</i> indicates that the item does not belong in your rowset.</li>
</ul>



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
 

 

