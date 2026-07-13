---
UID: NF:control.IMediaControl.Pause
title: IMediaControl::Pause (control.h)
description: The Pause method pauses all the filters in the filter graph.
helpviewer_keywords: ["IMediaControl interface [DirectShow]","Pause method","IMediaControl.Pause","IMediaControl::Pause","IMediaControlPause","Pause","Pause method [DirectShow]","Pause method [DirectShow]","IMediaControl interface","control/IMediaControl::Pause","dshow.imediacontrol_pause"]
old-location: dshow\imediacontrol_pause.htm
tech.root: dshow
ms.assetid: cfb875b7-cc4e-4ae2-8379-964d0e3ceb04
ms.date: 4/26/2023
ms.keywords: IMediaControl interface [DirectShow],Pause method, IMediaControl.Pause, IMediaControl::Pause, IMediaControlPause, Pause, Pause method [DirectShow], Pause method [DirectShow],IMediaControl interface, control/IMediaControl::Pause, dshow.imediacontrol_pause
req.header: control.h
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
 - IMediaControl::Pause
 - control/IMediaControl::Pause
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
 - IMediaControl.Pause
---

# IMediaControl::Pause


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>Pause</code> method pauses all the filters in the filter graph.



## -returns

Returns an <b>HRESULT</b> value. Possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The graph paused successfully, but some filters have not completed the state transition.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
All filters in the graph completed the transition to a paused state.

</td>
</tr>
</table>

## -remarks

Pausing the filter graph cues the graph for immediate rendering when the graph is next run. While the graph is paused, filters process data but do not render it. Data is pushed through the graph and processed by transform filters as far as buffering permits, but renderer filters do not render the data. However, video renderers display a static poster frame of the first sample.

If the method returns S_FALSE, call the <a href="/windows/desktop/api/control/nf-control-imediacontrol-getstate">IMediaControl::GetState</a> method to wait for the state transition to complete, or to check if the transition has completed. When you call <code>Pause</code> to display the first frame of a video file, always follow it immediately with a call to <b>GetState</b> to ensure that the state transition has completed. Failure to do this can result in the video rectangle being painted black.

If the method fails, it stops the graph before returning.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/control/nn-control-imediacontrol">IMediaControl Interface</a>



<a href="/windows/desktop/api/control/nf-control-imediacontrol-stopwhenready">IMediaControl::StopWhenReady</a>
