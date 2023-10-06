---
UID: NF:strmif.IMediaFilter.SetSyncSource
title: IMediaFilter::SetSyncSource (strmif.h)
description: The SetSyncSource method sets the reference clock.
helpviewer_keywords: ["IMediaFilter interface [DirectShow]","SetSyncSource method","IMediaFilter.SetSyncSource","IMediaFilter::SetSyncSource","IMediaFilterSetSyncSource","SetSyncSource","SetSyncSource method [DirectShow]","SetSyncSource method [DirectShow]","IMediaFilter interface","dshow.imediafilter_setsyncsource","strmif/IMediaFilter::SetSyncSource"]
old-location: dshow\imediafilter_setsyncsource.htm
tech.root: dshow
ms.assetid: a374c963-cc28-41f6-814d-7ffc6efc67a6
ms.date: 4/26/2023
ms.keywords: IMediaFilter interface [DirectShow],SetSyncSource method, IMediaFilter.SetSyncSource, IMediaFilter::SetSyncSource, IMediaFilterSetSyncSource, SetSyncSource, SetSyncSource method [DirectShow], SetSyncSource method [DirectShow],IMediaFilter interface, dshow.imediafilter_setsyncsource, strmif/IMediaFilter::SetSyncSource
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMediaFilter::SetSyncSource
 - strmif/IMediaFilter::SetSyncSource
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IMediaFilter.SetSyncSource
---

# IMediaFilter::SetSyncSource


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>SetSyncSource</code> method sets the reference clock.

## -parameters

### -param pClock [in]

Pointer to the clock's <a href="/windows/desktop/api/strmif/nn-strmif-ireferenceclock">IReferenceClock</a> interface, or <b>NULL</b>. If this parameter is <b>NULL</b>, the filter graph does not use a reference clock, and all filters run as quickly as possible.

## -returns

Returns S_OK if successful, or an <b>HRESULT</b> value indicating the cause of the error.

## -remarks

All the filters in the filter graph share the same reference clock, in order to stay synchronized. Stream time is calculated from the reference clock. Renderer filters use the reference clock to schedule when they render samples. If there is no reference clock, a renderer filter renders every sample as soon as it arrives.

This method is implemented by all DirectShow filters, and also by the Filter Graph Manager.

<h3><a id="Filter_Implementation"></a><a id="filter_implementation"></a><a id="FILTER_IMPLEMENTATION"></a>Filter Implementation</h3>
When the graph runs, the Filter Graph manager calls this method on every filter in the graph, to notify them of the graph reference clock. Use this method to store the <a href="/windows/desktop/api/strmif/nn-strmif-ireferenceclock">IReferenceClock</a> pointer. Increment the reference count on the stored pointer. Before the filter is removed from the graph, the Filter Graph Manager calls <b>SetSyncSource</b> again with the value <b>NULL</b>. Release the stored pointer and set it to <b>NULL</b>.

The <a href="/windows/desktop/DirectShow/cbasefilter">CBaseFilter</a> class implements this method; see <a href="/windows/desktop/DirectShow/cbasefilter-setsyncsource">CBaseFilter::SetSyncSource</a>.

Note that filters cannot use this method to select the graph clock. In filters, the only function of this method is to inform the filter of the clock that the graph is using. A filter can provide a reference clock by exposing the <a href="/windows/desktop/api/strmif/nn-strmif-ireferenceclock">IReferenceClock</a> interface. For more information, see <a href="/windows/desktop/DirectShow/time-and-clocks-in-directshow">Time and Clocks in DirectShow</a>.

<h3><a id="Application_Use"></a><a id="application_use"></a><a id="APPLICATION_USE"></a>Application Use</h3>
An application can override the default clock by calling <b>SetSyncSource</b> on the Filter Graph Manager. Do not do this unless you have a particular reason to prefer another clock. You can also set the graph not to use any reference clock, by calling <b>SetSyncSource</b> with the value <b>NULL</b>. You might do this to process samples as quickly as possible. For more information, see <a href="/windows/desktop/DirectShow/setting-the-graph-clock">Setting the Graph Clock</a>.

Applications should never call this method on filters.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nf-strmif-ifiltergraph-setdefaultsyncsource">IFilterGraph::SetDefaultSyncSource</a>



<a href="/windows/desktop/api/strmif/nn-strmif-imediafilter">IMediaFilter Interface</a>