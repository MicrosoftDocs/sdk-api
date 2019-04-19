---
UID: NF:searchapi.IRowsetEvents.OnRowsetEvent
title: IRowsetEvents::OnRowsetEvent (searchapi.h)
author: windows-sdk-content
description: Called by the indexer to notify clients of an event related to the client rowset.
old-location: search\_search_IRowsetEvents_OnRowsetEvent.htm
tech.root: search
ms.assetid: VS|SEARCH|~\search\wds3x\reference\ifaces\querying\irowsetevents\onrowsetevent.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IRowsetEvents interface [search],OnRowsetEvent method, IRowsetEvents.OnRowsetEvent, IRowsetEvents::OnRowsetEvent, OnRowsetEvent, OnRowsetEvent method [search], OnRowsetEvent method [search],IRowsetEvents interface, _search_IRowsetEvents_OnRowsetEvent, search._search_IRowsetEvents_OnRowsetEvent, searchapi/IRowsetEvents::OnRowsetEvent
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
 - IRowsetEvents.OnRowsetEvent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IRowsetEvents::OnRowsetEvent


## -description


Called by the indexer to notify clients of an event related to the client rowset.
            


## -parameters




### -param eventType [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Dd368862(v=VS.85).aspx">ROWSETEVENT_TYPE</a></b>

The event triggering the notification as the <a href="https://msdn.microsoft.com/en-us/library/Dd368862(v=VS.85).aspx">ROWSETEVENT_TYPE</a> enumeration.
        


### -param eventData [in]

Type: <b>REFPROPVARIANT</b>

The expected value of the event data for the event type.
        


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




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
 

 

