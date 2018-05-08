---
UID: NF:strmif.IMediaFilter.SetSyncSource
title: IMediaFilter::SetSyncSource
author: windows-driver-content
description: The SetSyncSource method sets the reference clock.
old-location: dshow\imediafilter_setsyncsource.htm
old-project: DirectShow
ms.assetid: a374c963-cc28-41f6-814d-7ffc6efc67a6
ms.author: windowsdriverdev
ms.date: 4/30/2018
ms.keywords: IMediaFilter interface [DirectShow],SetSyncSource method, IMediaFilter.SetSyncSource, IMediaFilter::SetSyncSource, IMediaFilterSetSyncSource, SetSyncSource, SetSyncSource method [DirectShow], SetSyncSource method [DirectShow],IMediaFilter interface, dshow.imediafilter_setsyncsource, strmif/IMediaFilter::SetSyncSource
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IMediaFilter.SetSyncSource
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IMediaFilter::SetSyncSource


## -description



The <code>SetSyncSource</code> method sets the reference clock.




## -parameters




### -param pClock [in]

Pointer to the clock's <a href="https://msdn.microsoft.com/9818c67d-dfbe-4498-a744-d2efaa4bfb58">IReferenceClock</a> interface, or <b>NULL</b>. If this parameter is <b>NULL</b>, the filter graph does not use a reference clock, and all filters run as quickly as possible.


## -returns



Returns S_OK if successful, or an <b>HRESULT</b> value indicating the cause of the error.




## -remarks



All the filters in the filter graph share the same reference clock, in order to stay synchronized. Stream time is calculated from the reference clock. Renderer filters use the reference clock to schedule when they render samples. If there is no reference clock, a renderer filter renders every sample as soon as it arrives.

This method is implemented by all DirectShow filters, and also by the Filter Graph Manager.

<h3><a id="Filter_Implementation"></a><a id="filter_implementation"></a><a id="FILTER_IMPLEMENTATION"></a>Filter Implementation</h3>
When the graph runs, the Filter Graph manager calls this method on every filter in the graph, to notify them of the graph reference clock. Use this method to store the <a href="https://msdn.microsoft.com/9818c67d-dfbe-4498-a744-d2efaa4bfb58">IReferenceClock</a> pointer. Increment the reference count on the stored pointer. Before the filter is removed from the graph, the Filter Graph Manager calls <b>SetSyncSource</b> again with the value <b>NULL</b>. Release the stored pointer and set it to <b>NULL</b>.

The <a href="https://msdn.microsoft.com/4610c8d6-9d7d-47ca-b1d5-0a867153a5f6">CBaseFilter</a> class implements this method; see <a href="https://msdn.microsoft.com/298039fc-dd38-4063-8752-2669b134b8ef">CBaseFilter::SetSyncSource</a>.

Note that filters cannot use this method to select the graph clock. In filters, the only function of this method is to inform the filter of the clock that the graph is using. A filter can provide a reference clock by exposing the <a href="https://msdn.microsoft.com/9818c67d-dfbe-4498-a744-d2efaa4bfb58">IReferenceClock</a> interface. For more information, see <a href="https://msdn.microsoft.com/7d883638-5ddb-48b9-9d0b-104944a151e9">Time and Clocks in DirectShow</a>.

<h3><a id="Application_Use"></a><a id="application_use"></a><a id="APPLICATION_USE"></a>Application Use</h3>
An application can override the default clock by calling <b>SetSyncSource</b> on the Filter Graph Manager. Do not do this unless you have a particular reason to prefer another clock. You can also set the graph not to use any reference clock, by calling <b>SetSyncSource</b> with the value <b>NULL</b>. You might do this to process samples as quickly as possible. For more information, see <a href="https://msdn.microsoft.com/23deab26-6c9a-4f94-b750-11c9b1a14ce3">Setting the Graph Clock</a>.

Applications should never call this method on filters.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/775e7136-f6d0-47bc-852f-1c5c88ad03bf">IFilterGraph::SetDefaultSyncSource</a>



<a href="https://msdn.microsoft.com/5c0060e8-a9e5-4141-a38d-9a1bc55cc91b">IMediaFilter Interface</a>
 

 

