---
UID: NN:strmif.IMediaFilter
title: IMediaFilter (strmif.h)
description: The IMediaFilter interface controls the streaming state of a filter.All DirectShow filters implement this interface.
old-location: dshow\imediafilter.htm
tech.root: DirectShow
ms.assetid: 5c0060e8-a9e5-4141-a38d-9a1bc55cc91b
ms.date: 12/05/2018
ms.keywords: IMediaFilter, IMediaFilter interface [DirectShow], IMediaFilter interface [DirectShow],described, IMediaFilterInterface, dshow.imediafilter, strmif/IMediaFilter
ms.topic: interface
f1_keywords:
- strmif/IMediaFilter
dev_langs:
- c++
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
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
api_name:
- IMediaFilter
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMediaFilter interface


## -description



The <code>IMediaFilter</code> interface controls the streaming state of a filter.

All DirectShow filters implement this interface. It provides methods for switching the filter between states (stopped, paused, and running); for retrieving the filter's current state; and for setting a reference clock. Applications should not call <code>IMediaFilter</code> methods on filters.

The <a href="https://docs.microsoft.com/windows/desktop/DirectShow/filter-graph-manager">Filter Graph Manager</a> also exposes this interface. Applications can use the <b>SetSyncSource</b> method to set the graph reference clock, and <b>GetSyncSource</b> to retrieve the clock. Applications should not call the other methods on this interface. Instead, use the corresponding methods on the <a href="https://docs.microsoft.com/windows/desktop/api/control/nn-control-imediacontrol">IMediaControl</a> interface.

The <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-ibasefilter">IBaseFilter</a> interface inherits from <code>IMediaFilter</code>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMediaFilter</b> interface inherits from <b>IPersist</b>. <b>IMediaFilter</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMediaFilter</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-imediafilter-getstate">GetState</a>
</td>
<td align="left" width="63%">
Retrieves the state of the filter (running, stopped, or paused).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-imediafilter-getsyncsource">GetSyncSource</a>
</td>
<td align="left" width="63%">
Retrieves the current reference clock.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-imediafilter-pause">Pause</a>
</td>
<td align="left" width="63%">
Pauses the filter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-imediafilter-run">Run</a>
</td>
<td align="left" width="63%">
Runs the filter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-imediafilter-setsyncsource">SetSyncSource</a>
</td>
<td align="left" width="63%">
Sets the reference clock for the filter or the filter graph.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-imediafilter-stop">Stop</a>
</td>
<td align="left" width="63%">
Stops the filter.

</td>
</tr>
</table> 

