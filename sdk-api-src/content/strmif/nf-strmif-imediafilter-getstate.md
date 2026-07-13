---
UID: NF:strmif.IMediaFilter.GetState
title: IMediaFilter::GetState (strmif.h)
description: The GetState method retrieves the filter's state (running, stopped, or paused).
helpviewer_keywords: ["GetState","GetState method [DirectShow]","GetState method [DirectShow]","IBaseFilter interface","GetState method [DirectShow]","IMediaFilter interface","IBaseFilter interface [DirectShow]","GetState method","IBaseFilter::GetState","IMediaFilter interface [DirectShow]","GetState method","IMediaFilter.GetState","IMediaFilter::GetState","IMediaFilterGetState","dshow.imediafilter_getstate","strmif/IBaseFilter::GetState","strmif/IMediaFilter::GetState"]
old-location: dshow\imediafilter_getstate.htm
tech.root: dshow
ms.assetid: b20ca3e9-bec2-4c6d-ba80-f4dae2f5a831
ms.date: 4/26/2023
ms.keywords: GetState, GetState method [DirectShow], GetState method [DirectShow],IBaseFilter interface, GetState method [DirectShow],IMediaFilter interface, IBaseFilter interface [DirectShow],GetState method, IBaseFilter::GetState, IMediaFilter interface [DirectShow],GetState method, IMediaFilter.GetState, IMediaFilter::GetState, IMediaFilterGetState, dshow.imediafilter_getstate, strmif/IBaseFilter::GetState, strmif/IMediaFilter::GetState
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
 - IMediaFilter::GetState
 - strmif/IMediaFilter::GetState
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
 - IMediaFilter.GetState
 - IBaseFilter.GetState
---

# IMediaFilter::GetState


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetState</b> method retrieves the filter's state (running, stopped, or paused).

## -parameters

### -param dwMilliSecsTimeout [in]

Time-out interval, in milliseconds. To block indefinitely, use the value <b>INFINITE</b>.

### -param State [out]

Receives a member of the [FILTER_STATE](/windows/desktop/api/strmif/ne-strmif-filter_state) enumerated type, indicating the filter's state.

## -returns

Returns an <b>HRESULT</b> value. Possible values include those shown in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_S_STATE_INTERMEDIATE</b></dt>
</dl>
</td>
<td width="60%">
Intermediate state.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_S_CANT_CUE</b></dt>
</dl>
</td>
<td width="60%">
The filter is active, but cannot deliver data.

</td>
</tr>
</table>

## -remarks

State transitions can be asynchronous. If the filter is transitioning to a new state, and the method times out before the transition completes, the method returns <b>VFW_S_STATE_INTERMEDIATE</b>.

If a filter cannot deliver data for some reason, it returns <b>VFW_S_CANT_CUE</b>. Live capture filters return this value while paused, because they do not deliver data in the paused state.

For more information, see <a href="/windows/desktop/DirectShow/data-flow-in-the-filter-graph">Data Flow in the Filter Graph</a>.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-ibasefilter">IBaseFilter</a>



<a href="/windows/desktop/api/strmif/nn-strmif-imediafilter">IMediaFilter Interface</a>