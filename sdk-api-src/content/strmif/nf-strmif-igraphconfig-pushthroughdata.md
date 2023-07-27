---
UID: NF:strmif.IGraphConfig.PushThroughData
title: IGraphConfig::PushThroughData (strmif.h)
description: The PushThroughData method pushes data through the filter graph to the specified pin.
helpviewer_keywords: ["IGraphConfig interface [DirectShow]","PushThroughData method","IGraphConfig.PushThroughData","IGraphConfig::PushThroughData","IGraphConfigPushThroughData","PushThroughData","PushThroughData method [DirectShow]","PushThroughData method [DirectShow]","IGraphConfig interface","dshow.igraphconfig_pushthroughdata","strmif/IGraphConfig::PushThroughData"]
old-location: dshow\igraphconfig_pushthroughdata.htm
tech.root: dshow
ms.assetid: f3d72a32-f43a-4a61-b25e-6d472aa629de
ms.date: 4/26/2023
ms.keywords: IGraphConfig interface [DirectShow],PushThroughData method, IGraphConfig.PushThroughData, IGraphConfig::PushThroughData, IGraphConfigPushThroughData, PushThroughData, PushThroughData method [DirectShow], PushThroughData method [DirectShow],IGraphConfig interface, dshow.igraphconfig_pushthroughdata, strmif/IGraphConfig::PushThroughData
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - IGraphConfig::PushThroughData
 - strmif/IGraphConfig::PushThroughData
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
 - IGraphConfig.PushThroughData
---

# IGraphConfig::PushThroughData


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>PushThroughData</code> method pushes data through the filter graph to the specified pin.

## -parameters

### -param pOutputPin [in]

Pointer to the <a href="/windows/desktop/api/strmif/nn-strmif-ipin">IPin</a> interface of an output pin in the filter graph.

### -param pConnection [in]

Pointer to the <a href="/windows/desktop/api/strmif/nn-strmif-ipinconnection">IPinConnection</a> interface of an input pin in the filter graph. This parameter can be <b>NULL</b>.

### -param hEventAbort [in]

Handle to an event. If the caller is a filter calling on one of its data processing threads, this parameter should be a handle to an event that will be signaled when the filter is put into a stopped state. Otherwise, this parameter can be <b>NULL</b>. For more information, see Remarks.

## -returns

Returns S_OK if successful. Otherwise, returns an error code that may be one of the following values, or others not listed.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Failed to allocate necessary memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
Could not find a candidate input pin.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_STATE_CHANGED</b></dt>
</dl>
</td>
<td width="60%">
Filter state changed during the operation.

</td>
</tr>
</table>

## -remarks

This method pushes through any pending data, from a specified output pin down to a specified input pin. Optionally, you can leave the input pin unspecified and let the method search the filter graph for the best candidate. Do not call this method from the thread that is pushing data.

If a filter calls this method on one of its own data processing threads, it creates the potential for a deadlock. The method obtains a lock on the filter graph, which can block the filter from stopping on receiving a call to <a href="/windows/desktop/api/strmif/nf-strmif-imediafilter-stop">IMediaFilter::Stop</a>. To prevent this situation, the method takes a handle to an event object provided by the filter. The filter should signal the event if it receives a call to its <b>Stop</b> method.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-igraphconfig">IGraphConfig Interface</a>